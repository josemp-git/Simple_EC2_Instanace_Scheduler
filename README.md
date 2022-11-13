# Simple EC2 Instance Scheduler

This simple solution deploys two AWS Lambda functions that will start and stop the EC2 instances of your choice by adding a specific tag. For this purpose, two Amazon EventBridge rules are created:

* One rule will execute the AWS Lambda function that will start all your tagged instances at 08:00 AM (CDT) from Monday to Friday.
* The second rule will execute the AWS Lambda function that will stop all your tagged instances at 20:00 (CDT) from Monday to Friday.

You can use this solution with those environments that are not required to be on 24/7 (e.g: dev and test) and save money.

## Instructions

1. Deploy the AWS CloudFormation template.
2. After deploying the AWS CloudFormation template, add the following tag to the Amazon EC2 instances that you want to start and stop automatically:

* Key = scheduled
* Value = true

You are set.

You can change the name and value of the tag to use when deploying the AWS CloudFormation template.

You can change the start/stop times and frequency of execution by modifying the Amazon EventBridge rules.

