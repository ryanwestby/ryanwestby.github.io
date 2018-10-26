---
title: Useful Serverless Plugins
layout: post
date: 2018-08-26 22:00
headerImage: false
tag:
- tech
- serverless
category: blog
author: ryanwestby
---

## serverless-plugin-additional-stacks
This plugin is useful if you have resources that you would like to keep separated from the CloudFormation stack of your project. For example, if you have an S3 Bucket or DynamoDB table with important data on it that you would like to persist in case your project were to be torn down.

## serverless-prune-plugin
By default, the Serverless Framework creates function versions for every deploy. The Serverless Framework does not purge previous versions from AWS, so the number of deployed versions can grow out of hand rather quickly. This plugin allows you to specify a certain number of versions to keep, while pruning the rest.
This plugin should be used on all projects that version functions.

## serverless-domain-manager
This plugin is used to create a custom domain that your lambda can deploy to. This is useful if you would like to use your own endpoint rather than the one that Serverless generates.

## serverless-plugin-aws-alerts
Allows CloudWatch alarms to be added to functions. This is likely useful in all production environments that would like to be notified of errors.

## serverless-plugin-canary-deployments
This is a handy plugin that adds traffic shifting with AWS CodeDeploy. For example, when deploying new code, you can specify that only a certain percentage of traffic gets shifted to the new code, and on no errors for a specified amount of time, the full 100% can be shifted.

## serverless-plugin-tracing
Enables AWS X-Ray for the entire Serverless stack or individual functions. There are several useful features of X-Ray, but a particularly good one is that it tracks invocation times, and can even track an entire chain of lambdas or requests. A segment of code can also be specified for X-Ray, if more detailed analysis on a piece of code is needed.

## serverless-plugin-existing-s3
Overcomes the CloudFormation limitation on attaching an event to an uncontrolled bucket
https://serverfault.com/questions/610788/using-cloudformation-with-an-existing-s3-bucket

## serverless-hooks-plugin
Adds hooks to Serverless lifecycle events. This is useful if hooks are needed before packaging the directory or before or after deployments.

## serverless-python-requirements
Automatically bundle dependencies from Pipfile / requirements.txt and make them available in your Lambda's PYTHONPATH. This is very useful on nearly on Serverless Python projects.

## serverless-ephemeral
Bundles stateless libraries into Lambda deployment artifacts.
This plugin can be used to build the TensorFlow package on a lambda.
More info here: https://github.com/Accenture/serverless-ephemeral/blob/master/docs/build-tensorflow-package.md

## serverless-finch
This plugin makes it very easy to deploy a simple static site to be hosted on an S3 bucket.

## serverless-express
Makes Express.js servers compatible with Serverless. A full Serverless REST API can be deployed using this plugin. 

## serverless-dotenv-plugin
Preload environment variables that are stored in a .env file into Serverless. This allows you to load environment variables into your lambda without needing to commit them to the repo.