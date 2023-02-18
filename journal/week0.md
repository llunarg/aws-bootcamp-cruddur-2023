# Week 0 — Billing and Architecture

 - ***Below are the activities assigned as part of week 0 of the Bootcamp. A brief documentation of each activity and evidence of each  as appropriate.***
 
 - ***Security considerations were taken into account in the user creation process (MFA), the "Authy" application was selected for token management due to its multi-device facility.***

 **1. Create of the Admin user.**

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

**4. Installed AWS CLI**

The AWS Command Line Interface (AWS CLI) is an open source tool that enables you to interact with AWS services using commands in your command-line shell. With minimal configuration, the AWS CLI enables you to start running commands that implement functionality equivalent to that provided by the browser-based AWS Management Console from the command prompt in your terminal program.

**Install or update the AWS CLI**

To update your current installation of AWS CLI, download a new installer each time you update to overwrite previous versions. Follow these steps from the command line to install the AWS CLI on Linux.

[Installing or updating the latest version of the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

**5. Create a Billing Alarm**

You can monitor your estimated AWS charges by using Amazon CloudWatch. When you enable the monitoring of estimated charges for your AWS account, the estimated charges are calculated and sent several times daily to CloudWatch as metric data.

Billing metric data is stored in the US East (N. Virginia) Region and represents worldwide charges. This data includes the estimated charges for every service in AWS that you use, in addition to the estimated overall total of your AWS charges.

The alarm triggers when your account billing exceeds the threshold you specify. It triggers only when the current billing exceeds the threshold. It doesn't use projections based on your usage so far in the month.

If you create a billing alarm at a time when your charges have already exceeded the threshold, the alarm goes to the ALARM state immediately.

In this procedure, you create an alarm that sends a notification when your estimated charges for AWS exceed a defined threshold.

[Creating a billing alarm to monitor your estimated AWS charges
](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/monitor_estimated_charges_with_cloudwatch.html#creating_billing_alarm_with_wizard)

![My billing Alarm](https://github.com/llunarg/aws-bootcamp-cruddur-2023/blob/main/journal/assets/5%20Create%20a%20Billing%20Alarm.png)

**6 Create a Budget**

You can create budgets to track and take action on your costs and usage. You can also create budgets to track your aggregate Reserved Instance (RI) and Savings Plans utilization and coverage. By default, single accounts, the management account, and member accounts in an organization can create budgets.

When you create a budget, AWS Budgets provides a Cost Explorer graph to help you see your incurred costs and usage. If you didn't enable Cost Explorer yet, this graph is blank and AWS Budgets will enable Cost Explorer when you create your first budget. You can create your budget without enabling Cost Explorer. It can take up to 24 hours for this graph to appear after you or AWS Budgets enable Cost Explorer.

[Creating a cost budget](https://docs.aws.amazon.com/cost-management/latest/userguide/create-cost-budget.html)

![My budget](https://github.com/llunarg/aws-bootcamp-cruddur-2023/blob/main/journal/assets/6%20Create%20a%20Budget.png)

**7. GipPod Credentials Configuration**

tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -or "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
vscode:
  extensions:
    - 42Crunch.vscode-openapi
   
**8 Practica aplicación Lucidchart**

[Logical Design](https://lucid.app/lucidchart/6e9d3d7b-97f3-44cb-8925-5d2b77fe1210/edit?viewport_loc=-163,-33,2219,1067,0_0&invitationId=inv_0808bc66-fb91-4d12-9665-23022966baa6)

**Note: You can see GipPod button in the repository**
