# Simple EC2 Instance Scheduler

This AWS CloudFormation template deploys two AWS Lambda functions that will start and shutdown the EC2 instances of your choice. You just need to tag the EC2 instances that you want to schedule. This AWS CloudFormation template also configures two Amazon EventBridge rules:

* One rule will execute the AWS Lambda function that will start all your tagged instances at 08:00 AM (CDT) from Monday to Friday.
* The second rule will execute the AWS Lambda function that will shutdown all your tagged instances at 20:00 (CDT) from Monday to Friday.

Deploy the this AWS CloudFormation template and add the following tag to your Amazon EC2 instances:

* Name = scheduled
* Value = true

You are set.

