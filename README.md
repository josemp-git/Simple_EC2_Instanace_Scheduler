# Simple EC2 Instance Scheduler

This AWS CloudFormation template deploys two AWS Lambda functions that will start and stop the EC2 instances of your choice by adding an specific tag. This AWS CloudFormation template also configures two Amazon EventBridge rules:

* One rule will execute the AWS Lambda function that will start all your tagged instances at 08:00 AM (CDT) from Monday to Friday.
* The second rule will execute the AWS Lambda function that will stop all your tagged instances at 20:00 (CDT) from Monday to Friday.

After deploying the AWS CloudFormation template, add the following tag to the Amazon EC2 instances that you want to start and stop automatically:

* Name = scheduled
* Value = true

You are set.

You can change the name and value of the tag to use when deploying the AWS CloudFormation template.

You can modify the start and shutdown times directly in Amazon EventBridge.

