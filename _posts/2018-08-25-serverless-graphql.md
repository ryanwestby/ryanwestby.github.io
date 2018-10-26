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

<!-- Begin MailChimp Signup Form -->
<link href="//cdn-images.mailchimp.com/embedcode/classic-10_7.css" rel="stylesheet" type="text/css">
<style type="text/css">
	#mc_embed_signup{background:#fff; clear:left; font:14px Helvetica,Arial,sans-serif; }
	/* Add your own MailChimp form style overrides in your site stylesheet or in this style block.
	   We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. */
</style>
<div id="mc_embed_signup">
<form action="https://westby.us19.list-manage.com/subscribe/post?u=4ce1d2eb2422f24f44b2af88c&amp;id=bec4940a18" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
    <div id="mc_embed_signup_scroll">
	<h2>Want me to let you know when I write again?</h2>
<div class="indicates-required"><span class="asterisk">*</span> indicates required</div>
<div class="mc-field-group">
	<label for="mce-EMAIL">Email Address  <span class="asterisk">*</span>
</label>
	<input type="email" value="" name="EMAIL" class="required email" id="mce-EMAIL">
</div>
<div class="mc-field-group">
	<label for="mce-MMERGE6">Categories </label>
	<input type="text" value="Tech" name="MMERGE6" class="" id="mce-MMERGE6">
</div>
	<div id="mce-responses" class="clear">
		<div class="response" id="mce-error-response" style="display:none"></div>
		<div class="response" id="mce-success-response" style="display:none"></div>
	</div>    <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
    <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="b_4ce1d2eb2422f24f44b2af88c_bec4940a18" tabindex="-1" value=""></div>
    <div class="clear"><input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button"></div>
    </div>
</form>
</div>
<script type='text/javascript' src='//s3.amazonaws.com/downloads.mailchimp.com/js/mc-validate.js'></script><script type='text/javascript'>(function($) {window.fnames = new Array(); window.ftypes = new Array();fnames[0]='EMAIL';ftypes[0]='email';fnames[6]='MMERGE6';ftypes[6]='text';}(jQuery));var $mcj = jQuery.noConflict(true);</script>
<!--End mc_embed_signup-->