# Hello World Lambda Java

This is a "sam init" template to generate a "Hello World" AWS Lambda function, implemented in Java.

This is an alternative to the similar project at https://github.com/symphoniacloud/sam-init-HelloWorldLambdaJava . 
This version produces an artifact using a zip format, rather than an "Uberjar", and also creates a "reproducible" artifact.

For details on install the SAM CLI, see https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html

To generate a project using this template, run:

```
$ sam init --location gh:symphoniacloud/sam-templates/HelloWorldLambdaJava
```