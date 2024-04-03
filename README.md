# AWS CI/CD APP

This project is a demonstration of setting up a CI/CD pipeline on AWS for automated deployment.


![1](https://github.com/tushar10898/aws-ci-cd-project/assets/165803170/78ce1f0c-5531-4e1e-ad63-d675dcb1dabd)


## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Setup](#setup)
4. [CI/CD Pipeline](#ci-cd-pipeline)
5. [Troubleshooting](#troubleshooting)
6. [Contributing](#contributing)

## Introduction
The "AWS CI/CD APP" project showcases how to implement a continuous integration and continuous deployment (CI/CD) pipeline using AWS services. It automates the process of building, testing, and deploying the application to AWS infrastructure.

## Features
- Automated deployment process
- Integration with AWS services for CI/CD
- Easy setup and configuration

## Setup
To set up the "AWS CI/CD APP" project:
1. Clone the repository to your local machine.
2. Create a basic HTML file for the application.
3. Create an `appspec.yml` file to define the deployment process.
4. Create a `buildspec.yml` file to define the build process.
5. Write a script to set up NGINX.
6. Push these files (HTML, `appspec.yml`, `buildspec.yml`, NGINX script) to AWS CodeCommit using Visual Studio Code.
7. Configure AWS credentials and permissions for CodeBuild and CodeDeploy.
8. Set up an S3 bucket as an artifact store for CodeBuild.
9. Create an EC2 instance to serve as the compute resource for CodeDeploy.

## CI/CD Pipeline
The CI/CD pipeline for this project is built using AWS CodePipeline, AWS CodeBuild, and AWS CodeDeploy. It consists of the following stages:
1. **Source**: Fetches the source code from the repository in AWS CodeCommit.
2. **Build**: Executes the build process defined in the `buildspec.yml` file using AWS CodeBuild. The artifacts are stored in an S3 bucket.
3. **Deploy**: Deploys the application to the EC2 instance using AWS CodeDeploy, based on the `appspec.yml` file.

### Configuration
1. Configure AWS credentials and permissions.
2. Set up a CodePipeline project and define the pipeline structure.
3. Configure CodeBuild to build and package the application.
4. Define deployment settings in CodeDeploy.

## Troubleshooting
If you encounter deployment errors related to the CodeDeploy agent, follow these steps:
1. SSH into your EC2 instance.
2. Paste the `codedeployagent.sh` script provided in the repository in vim editor [plese edit region of aws deploy and s3,in my case it was us-east-1 ]
3. Run the script to set up the CodeDeploy agent.
4. Make sure codedeploy-agent service up and running
5. Retry the deployment process.

## Note
Ensure that all AWS services used, such as EC2 and S3, are in the same region to avoid compatibility issues.

## Contributing
Contributions to the "AWS CI/CD APP" project are welcome! To contribute:
1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

---

Feel free to modify and expand upon this template as needed for your project.
