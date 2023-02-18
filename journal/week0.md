# Week 0 — Billing and Architecture

 **1. Creation of the Admin user.**

The "admin" user has special privileges within the AWS platform. An AWS Identity and Access Management (IAM) user is an entity that you create in AWS. The IAM user represents the human user or workload who uses the IAM user to interact with AWS. A user in AWS consists of a name and credentials. An IAM user with administrator permissions is not the same thing as the AWS account root user. You can use the AWS Management Console to create IAM users.

**See:** [Creating IAM Users](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html#id_users_create_console)

![Creating Userd Admin](https://github.com/llunarg/aws-bootcamp-cruddur-2023/blob/main/journal/assets/1%20Creation%20of%20the%20Admin%20user..png)

**2. Use CloudShell**

AWS CloudShell is a browser-based, pre-authenticated shell that you can launch directly from the AWS Management Console. You can run AWS CLI commands against AWS services using your preferred shell, such as Bash, PowerShell, or Z shell. 

When you launch AWS CloudShell, a compute environment that's based on Amazon Linux 2 is created. Within this environment, you can access an extensive range of pre-installed development tools, options for uploading and downloading files, and file storage that persists between sessions.

The following tutorials show you how to perform tasks using AWS CloudShell - 

See: [AWS CloudShell tutorials](https://docs.aws.amazon.com/cloudshell/latest/userguide/tutorials.html)

![Using my CloudShell](https://github.com/llunarg/aws-bootcamp-cruddur-2023/blob/main/journal/assets/2%20Use%20CloudShell.png)

**3. Generate AWS Credentials**

AWS requires different types of security credentials, depending on how you access AWS and what type of AWS user you are. For example, you use sign-in credentials for the AWS Management Console while you use access keys to make programmatic calls to AWS. Also, each identity you use, whether it be the account root user, an AWS Identity and Access Management (IAM) user, an AWS IAM Identity Center (successor to AWS Single Sign-On) user, or a federated identity has unique credentials within AWS.

**Considerations and alternatives for long-term access keys**

 - Don't embed long-term access keys and secret access keys in your
   application code or in a code repository.   
  
 - Use IAM roles to generate temporary security credentials whenever   
   possible. 
   
 - Use alternatives to long-term access keys for the AWS Command Line   
   Interface (AWS CLI) or the aws-shell.   
   
 - AWS CLI Version 2 integration with AWS IAM Identity Center (successor
   to AWS Single Sign-On) (IAM Identity Center).   
   
 - Don't create long-term access keys for human users who need access to
   applications or AWS services

![Access keys](https://github.com/llunarg/aws-bootcamp-cruddur-2023/blob/main/journal/assets/3%20Generate%20AWS%20Credentials.png)



