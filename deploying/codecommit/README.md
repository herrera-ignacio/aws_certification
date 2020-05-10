# CodeCommit

![codecommit](./codecommit.png)

> Storing our code

* Overview
* Security
* Notifications

## Overview

* __Version control__ (Git)
* Private Git Repositories
* No size limits (scale seamlessly)
* Fully managed, highly available
* Code only in AWS Cloud Account => increased security and compliance
* Secure (encrypted, access control, etc)
* Integrated with Jenkins, CodeBuild and other CI tools.

## Security

* Interactions are done using Git standard
* Authentication in GIT:
    * SSH
    * HTTPS
    * MFA
* Encryption
    * Automatically encrypted at rest using KMS
    * Encrypted in transit (cna only use HTTPS/SSH)
* Cross Account access:
    * Do not share SSH keys or AWS credentials
    * Use IAM Role and AWS STS (with AssumeRole API)

## Notifications

* Trigger notifications using __AWS SNS or AWS Lambda__:
    * Deletion of branches
    * Trigger for pushes in master branch
    * Notify external Build System
    * Trigger AWS Lamda function to perform codebase analysis (maybe credentials got commited?)
* Trigger notifications using __AWS CloudWatch Event Rules__:
    * Trigger for pull request updates (created/updated/deleted/commented)
    * Commit comments events
    * CloudWatch Event Rules goes into an SNS topic