# Micronaut AWS fuction
Implemented in three ways
1. V1 using FunctionInitializer
2. V2 using MicronautRequestHandler (Standard and the latest) - Needs a memory of 256MB although it uses only 93 MB. Need to check that.
3. V3 using java.util.function.Function - Seems to be an extension of the MicronautRequestHandler variety but does not work when the @FunctionBean is anything other than "test"

I am not sure how I created this project but i think i used this:
```
mn create-app aws-function --build maven --features aws-lambda-custom-runtime
```

Used the following commands
```
sam build
sam local invoke <Function Name> -e <Event file name>
```

P.S. Tried the constructor injection and that did not seem to work with the MicronautRequestHandler. Have to see later
P.S. Has temp code for API gateway. Did not work. https://micronaut-projects.github.io/micronaut-aws/latest/guide/#apiProxy
     Again something to be checked.
## Feature aws-lambda documentation

- [Micronaut AWS Lambda Function documentation](https://micronaut-projects.github.io/micronaut-aws/latest/guide/index.html#lambda)
