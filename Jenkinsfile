def server = Artifactory.server "artifactory-elyxor"
def buildInfo = Artifactory.newBuildInfo()
def rtGradle = Artifactory.newGradleBuild()

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: scm.branches,
                    extensions: scm.extensions + [[$class: 'LocalBranch'], [$class: 'WipeWorkspace']],
                    userRemoteConfigs: scm.userRemoteConfigs
                ])
            }
        }

        stage('Configure Aritfactory') {
            steps {
                script {
                    rtGradle.useWrapper = true

                    if(env.BRANCH_NAME == 'master') {
                        rtGradle.deployer repo: 'libs-release-local', server: server
                        rtGradle.resolver repo: 'libs-release', server: server
                    } else {
                        rtGradle.deployer repo: 'bins-snapshot-local', server: server
                        rtGradle.resolver repo: 'libs-snapshot', server: server
                    }
                    rtGradle.deployer.deployArtifacts = false // Disable artifacts deployment during Gradle run
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    rtGradle.run buildFile: 'build.gradle', tasks: 'build'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    if (!env.BRANCH_NAME.startsWith('PR-')) {
                      if(env.BRANCH_NAME == 'master') {
                          rtGradle.run buildFile: 'build.gradle', tasks: 'setReleaseVersion artifactoryPublish', buildInfo: buildInfo
                      }
                      else {
                          rtGradle.run buildFile: 'build.gradle', tasks: 'artifactoryPublish', buildInfo: buildInfo
                      }

                      rtGradle.deployer.deployArtifacts buildInfo
                    }
                }
            }
         }

         stage('Publish build info') {
            steps {
                script {
                    server.publishBuildInfo buildInfo
                }
            }
         }
    }
}
