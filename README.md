# kodey-cloudformation-sample

This repository is an example Kodey.ai Coding Agent Workflow

## Objectives

In this sample, we will explore how Kodey.ai can create cloudformation templates.

## Project Setup & Steps 

1. Signup for a new Kodey.ai account or login to your existing Kodey.ai environmenty (link-here)
2. Configure your Kodey.ai integrations to the desired issue tracker and cloud git provider.
3. Fork this repository, and clone it to the cloud git provider of your choosing (Github, Azure DevOps, Bitbucket)
4. Create the sample issue / work item in your issue tracker. Copy and Paste the issue description from below.
5. Execute the below prompt in the Kodey.ai chat UI
6. Validate the commits and pull requests in your cloud git provider

### SAMPLE PROMPT - Github Tools (Making Cloudformation Template)
```
    branch name to create: feature/aws-cloudformation-implementation-v1

    Information to agent: Do as the steps below are defined one by one. You are working in github repo so make sure to use tools related to github repo.
    NOTE: You should write the actual implementation of code not just comments.

    SCENARIO: You are working in a project in aws where it requires api gateway, sqs, lambda, dynamodb, rds and s3. The process looks like this: 
        First an api gateway is created which triggers a lambda function. The lambda function sends the data to sqs. 
        The sqs triggers another lambda function which sends the data to dynamodb and rds. 
        The dynamodb and rds are connected to s3. The s3 is used to store the data. 
        The data is then sent back to the api gateway.
        Now you have to create a cloudformation template to implement the above scenario.

    Steps:

    step 1: Using GithubCreateNewBranch tool, Create a new branch with name <branch name to create> first and then do the steps below.

    step 2: Using GithubCreateNewFile tool, Create a new file inside cloudformation-sample-v1 directory, the file should be called cloudformation.yaml. The file should have the cloudformation template to implement the above scenario.
    Make sure to use the correct resources and their properties to implement the scenario. Also, make sure to use the correct properties and their values. And use the correct references where required. The cloudformation template should be in yaml format.
    Make sure to use appropriate networking and security configurations like vpce, security groups, etc.  

    step 3: Using GithubCreateNewFile tool, Create a new file called README.md inside cloudformation-sample-v1 directory and add the description of the cloudformation template created in the above step.

    step 4: Using GithubCreatePullRequest tool, create a new Pull Request from the above created branch with title "CloudFormation Sample V1 Added".

```

### SAMPLE PROMPT - Azure DevOps Tools (Cloudformation Template)
```
    branch name to create: feature/aws-cloudformation-implementation-v1

    Information to agent: Do as the steps below are defined one by one. You are working in azure repo so make sure to use tools related to azure repo.
    NOTE: You should write the actual implementation of code not just comments.

    SCENARIO: You are working in a project in aws where it requires api gateway, sqs, lambda, dynamodb, rds and s3. The process looks like this: 
        First an api gateway is created which triggers a lambda function. The lambda function sends the data to sqs. 
        The sqs triggers another lambda function which sends the data to dynamodb and rds. 
        The dynamodb and rds are connected to s3. The s3 is used to store the data. 
        The data is then sent back to the api gateway.
        Now you have to create a cloudformation template to implement the above scenario.

    Steps:

    step 1: Using AzureDevopsBranchesCreateBranch tool, Create a new branch with name <branch name to create> first and then do the steps below.

    step 2: using AzureDevopsRepositoryCreateNewFile tool, Create a new file inside cloudformation-sample-v1 directory, the file should be called cloudformation.yaml. The file should have the cloudformation template to implement the above scenario.
    Make sure to use the correct resources and their properties to implement the scenario. Also, make sure to use the correct properties and their values. And use the correct references where required. The cloudformation template should be in yaml format.
    Make sure to use appropriate networking and security configurations like vpce, security groups, etc.  

    step 3: using AzureDevopsRepositoryCreateNewFile tool, Create a new file called README.md inside cloudformation-sample-v1 directory and add the description of the cloudformation template created in the above step.

    step 4: using AzureDevopsPullRequestsCreatePullRequest tool, create a new Pull Request from the above created branch with title "CloudFormation Sample V1 Added".

    step 5: using AzureDevopsIssuesUpdateIssue tool, update the issue status to done.
```

### SAMPLE PROMPT - Jira / Bitbucket (Making Project That hits API requests extract data and define serverless file)
```
    branch name to create: feature/aws-cloudformation-implementation-v1

    Information to agent: Do as the steps below are defined one by one. You are working in bitbucket repo so make sure to use tools related to bitbucket repo.
    NOTE: You should write the actual implementation of code not just comments. 

    SCENARIO: You are working in a project in aws where it requires api gateway, sqs, lambda, dynamodb, rds and s3. The process looks like this: 
        First an api gateway is created which triggers a lambda function. The lambda function sends the data to sqs. 
        The sqs triggers another lambda function which sends the data to dynamodb and rds. 
        The dynamodb and rds are connected to s3. The s3 is used to store the data. 
        The data is then sent back to the api gateway.
        Now you have to create a cloudformation template to implement the above scenario.

    Steps:

    step 1: Using BitBucketCreateNewBranch tool, Create a new branch with name <branch name to create> first and then do the steps below.

    step 2: Using BitBucketWriteCode tool, Create a new file inside cloudformation-sample-v1 directory, the file should be called cloudformation.yaml. The file should have the cloudformation template to implement the above scenario.
    Make sure to use the correct resources and their properties to implement the scenario. Also, make sure to use the correct properties and their values. And use the correct references where required. The cloudformation template should be in yaml format.
    Make sure to use appropriate networking and security configurations like vpce, security groups, etc.  

    step 3: Using BitBucketWriteCode tool, Create a new file called README.md inside cloudformation-sample-v1 directory and add the description of the cloudformation template created in the above step.

    step 4: Using BitBucketCreateNewPullRequest tool, create a new Pull Request from the above created branch with title "CloudFormation Sample V1 Added".

    step 5: Update this jira issue status to done.

```

## Once you have set the description of the issue in your relavant system. You need to use kodey UI Chat and execute below statement to get the work done. 

### Github Issue and Github Repo
```
   Get the issue with id <issue_id> from github repo and do as the description of the issue says.
```

### Azure Repo Issue and Azure Repo
```
   Get the issue with id <issue_id> from azure repo and do as the description of the issue says.
```

### Jira Issue and Bitbucket Repo
```
   Get the issue with id <issue_id> from bitbucket repo and do as the description of the issue says.
```

## Confirming Successful Sample Outputs

1. Confirm that the branch was created on the issue / work item
2. Confirm that the code created in the associated pull request contains the following
3. Confirm that the work item/issue/ticket in your relevant issue tracking platform is updated.