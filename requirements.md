Lab 3 - CloudFormation + AWS CodePipeline

Automated Infrastructure Deployment with AWS CloudFormation and CodePipeline

Objective:
To set up an automated CI/CD pipeline using AWS CodePipeline that provisions AWS resources using CloudFormation.

Lab Requirements:
Create a Simple CloudFormation Template

Define a CloudFormation YAML or JSON template that creates an S3 bucket.
Include parameters for bucket name and versioning (Enabled/Suspended).
Test your template locally using the AWS CLI (aws cloudformation validate-template).
Set Up a CodeCommit Repository

Create a new GitHub repository and push your CloudFormation template to the repository.
Make sure the template is on a specific branch (e.g., main or deploy).
Connect Your CodePipeline's Source action to this GitHub Repository of yours.
Configure CodePipeline

In AWS CodePipeline, create a new pipeline with the following stages:
Source: Connect to your CodeCommit repository and monitor the chosen branch.
Deploy: Use AWS CloudFormation as the deploy provider. Set the stack name and select your template file.
Automate Deployment Triggers

Set up the pipeline to trigger automatically whenever changes are pushed to the repository.
Test the pipeline by making a minor edit in the template and pushing it to the repository
Edit could be an addition of a New AWS Service of your choice
OR some changes to an existing resource.
Verify and Clean Up Resources

Confirm the creation of the S3 bucket in the AWS Management Console.
Delete the stack after verification to avoid any unwanted costs.
Grading Criteria:
Correct CloudFormation Template (20%)
Proper Setup and Connection of CodeCommit to CodePipeline (20%)
CodePipeline Stages Setup and Automated Trigger (20%)
Successful Deployment and Verification (20%)
Resource Cleanup and Documentation (20%)
Submission:
A brief summary of each step, along with screenshots of the created pipeline, the deployed S3 bucket and/or other AWS service, and the CodePipeline run logs.
