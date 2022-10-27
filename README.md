# Side project - AWS Lamdba function and Layers with SAM Applications

### Lamdba function introduction
Serverless compute services, or Functions as a Service (FaaS), e.g. AWS Lambda, provide a cost effective, scalable, and agile way to run scripts or programs on a schedule.
We will run Python code  using AWS Lambda.

### AWS Lambda layers V
You can configure your Lambda function to pull in additional code and content in the form of layers. A layer is a ZIP archive that contains libraries, a custom runtime, or other dependencies. With layers, you can use libraries in your function without needing to include them in your deployment package.

Layers let you keep your deployment package small, which makes development easier. You can avoid errors that can occur when you install and package dependencies with your function code.

### AWS Serverless Application Model (SAM) introduction
The AWS Serverless Application Model (SAM) is an open-source framework for building serverless applications. It provides shorthand syntax to express functions, APIs, databases, and event source mappings. With just a few lines per resource, you can define the application you want and model it using YAML. During deployment, SAM transforms and expands the SAM syntax into AWS CloudFormation syntax, enabling you to build serverless applications faster.

AWS SAM templates simplify the writing of infrastructure as code when deploying Cloudformation resources. 

The article main tool we will be using is the AWS Serverless Application Model Command Line Interface (SAM CLI).

# Installing the AWS SAM CLI on macOS
[Installing the AWS SAM CLI on macOS](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install-mac.html)

The following steps help you to install and configure the required prerequisites for using the AWS SAM CLI on your macOS host:
1. Create an AWS account.
2. Configure IAM permissions.
3. Install Docker. Note: Docker is only a prerequisite for testing your application locally.
4. Install Homebrew.
5. Install the AWS SAM CLI.


# Side project
This is a sample template for AWS - Below is a brief explanation of what we have generated for you:

```bash
.
├── README.md                   <-- This instructions file
├── event.json                  <-- API Gateway Proxy Integration event payload
├── hello_world                 <-- Source code for a lambda function
│   ├── __init__.py
│   ├── app.py                  <-- Lambda function code
│   ├── requirements.txt        <-- Lambda function code
├── samTemplate.yaml               <-- SAM Template
└── tests                       <-- Unit tests
    └── unit
        ├── __init__.py
        └── test_handler.py
```

# IAM: run_lambda_role Role
