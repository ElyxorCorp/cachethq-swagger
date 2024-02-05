# cachethq-swagger
Swagger API and client-library generation for https://cachethq.io

Using a OpenAPI v2.0 swagger file, this project generates api client libraries in multiple 

## Java
- generator library: okhttp-gson
- publish location: Elyxor Artifactory (not currently publicly availale)

To use the java client library, clone the repo, run `./gradlew build`, go into the `generated` folder and run `./gradlew build`.  
The generated java project currently creates a gradle 2.6 build which requires JDK 8 to build. 

## Python
- publish location: [PyPI](https://pypi.org/project/cachethq-client/) 
- generated API docs: https://github.com/ElyxorCorp/cachethq-swagger/blob/dev/api-doc/README.md 