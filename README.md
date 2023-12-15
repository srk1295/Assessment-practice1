Deploying an Application on AWS cloud:
=====================================

Application type web app, mobile app, desktop app, etc.,

however here is a general outline for deploying an application in AWS

prepare an application
ensure all code, dependencies and resources are bundled together. consider containerization with docker or a build tool like Maven or Gradle.
Configure Environment variables: define database connections, API keys and other setting specific to your AWS environment. Store them securely using AWS secrets Manager.
Version your application: implement a version control system like git to track changes and enable rollbacks if needed.

Choose an Deployment method:
Manual: infrastrucrure, create and configure resource like EC2 instance, security groups and load balancers.

Set an AWS environment:
Create an AWS account,
Configure security settings: Set up IAM roles for access control, VPCs for network isolation and security groups for Instances restrictions.
Allocate resources: choose the appropriate EC2 instance type, ECS cluster configuration, or Lambda function memory and timeout based on your application's requirments.

Deploy your applications:
Manula deployment: Launch EC2 instances, install dependencies, configure an application and start it.

Monitor and manage Application:
CloudWatch: monitor an application health, performance metrics and logs, set up alarms for critical events.
Auto Scaling Automatically adjust a resources (EC2 instances, Lambda functions) based on Traffic demands, optimizing cost and performance.
Updates and maintenance: implement a CICD pipeline for automated deployments and updates, Regularly patch dependencies and perform security scans.

##############################################################################################################################


![2d digram of deploying the cloud](https://github.com/srk1295/Assessment-practice1/assets/6206490/4e446ec0-5d75-4c68-9a4f-1081a7ad2c3b)


##############################################################################################################################

Application built process:
=========================

A source code will be pulled from the github to build a pipeline, 
From jenkins will build a pipeline in declarative method and  maven stage checks for the 'syntax error' on the built source code.
Sonarqube is used to check the vulnerabilities on the project to convert into distributable format.
OWASP tool is used to check the dependency of the var/Jar files of the project.
Nexus repository is a central platform functions with a multiple artifacts for storing the source code 
Docker is used to create Dockerfile from the maven build packages. 
The Dockerfile will build images and pushed to dockerhub for repository as in public or private. 
Docker container will be running by pulling the images from the dockerhub with an exposed port value defined under the dockerfile,
Monitoring tools like cloudwatch will be used for graphical representation.
Hence the build container will go live with the server, by QA teams for error free checks on the built application.
finally job completes with Testing and validation as job completed with no errors.
#############################################################################################################################
