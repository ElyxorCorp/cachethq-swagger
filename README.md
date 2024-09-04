# cachethq-swagger
Swagger API and client-library generation for https://cachethq.io

Using a OpenAPI v2.0 swagger file, this project generates api client libraries in multiple languages

## Java
- generator library: okhttp-gson
- publish location: Elyxor Artifactory (not currently publicly available)

To use the java client library, clone the repo, run `./gradlew build`, go into the `generated` folder and run `./gradlew build`.  

## Python
- publish location: [PyPI](https://pypi.org/project/cachethq-client/) 
