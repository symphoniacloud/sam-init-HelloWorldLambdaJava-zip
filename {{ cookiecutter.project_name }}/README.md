# {{ cookiecutter.project_name }}

Creates and deploys a "Hello World" AWS Lambda function, implemented in Java.

The output artifact is "reproducible" - it will be identical for the same source inputs - and also uses
a zip file format rather than an "Uberjar".

## Prerequisites

* Created: An AWS account, and an S3 bucket for storing temporary deployment artifacts (referred to as $CF_BUCKET below)
* Installed: AWS CLI, Maven, SAM CLI
* Configured: AWS credentials in your terminal

## Usage

To build:

```
$ mvn package
```

To deploy:

```
$ sam package --s3-bucket $CF_BUCKET --output-template-file target/packaged-template.yaml
$ sam deploy --template-file target/packaged-template.yaml --stack-name {{ cookiecutter.project_name }} --capabilities CAPABILITY_IAM
```

To test:

The above will create a new function in Lambda, so you can test via the Lambda web console,
or via the CLI using `aws lambda invoke`.

## More Information

Please see https://github.com/symphoniacloud/sam-init-HelloWorldLambdaJava-zip for more information.
