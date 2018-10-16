node {
    def server
    def buildInfo
    def rtGradle

    stage ('Checkout') {
        checkout([
            $class: 'GitSCM',
            branches: scm.branches,
            extensions: scm.extensions + [[$class: 'LocalBranch'], [$class: 'WipeWorkspace']],
            userRemoteConfigs: [[credentialsId: 'elx-bot', url: 'git@github.com:ElyxorCorp/cachethq-swagger.git']],
            doGenerateSubmoduleConfigurations: false
        ])
    }

    stage ('Artifactory configuration') {
        server = Artifactory.server "artifactory-elyxor"

        rtGradle = Artifactory.newGradleBuild()
        rtGradle.tool = 'gradle'
        rtGradle.useWrapper = true
        rtGradle.deployer repo: (env.BRANCH_NAME=='release' ? 'bins-release-local' : 'bins-snapshot-local'), server: server
        rtGradle.resolver repo: (env.BRANCH_NAME=='release' ? 'libs-release' : 'libs-snapshot'), server: server
        rtGradle.deployer.deployArtifacts = false // Disable artifacts deployment during Gradle run

        buildInfo = Artifactory.newBuildInfo()
    }

    stage ('Test') {
        rtGradle.run buildFile: 'build.gradle', tasks: 'clean test'
    }

    stage ('Deploy') {
        if (!env.BRANCH_NAME.startsWith('PR-')) {
            if (env.BRANCH_NAME == 'master') {
                rtGradle.run buildFile: 'build.gradle', tasks: 'setReleaseVersion artifactoryPublish', buildInfo: buildInfo
            }
            else {
                rtGradle.run buildFile: 'build.gradle', tasks: 'artifactoryPublish', buildInfo: buildInfo
            }
            rtGradle.deployer.deployArtifacts buildInfo
        }
    }

    stage ('Publish build info') {
        server.publishBuildInfo buildInfo
    }
}
