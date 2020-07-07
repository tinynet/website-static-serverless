# Serverless project for hosting a static website

## Instructions

* Create from basic template, language not important: sls create -t hello-world -n website-static -p website-static
* Install s3 sync plugin: 
(https://www.serverless.com/plugins/serverless-s3-sync)
sls plugin install -n serverless-s3-sync
-> added to serverless.yaml
* remove handler.js, and function sections from serverless.yaml, we don't need functions
* node_modules are ignored
* create pages directory and pages/index.html
* create S3 bucket resource
* add S3 bucket policy for public access

## Troubleshoot

- sls -v
- enable debug output: export SLS_DEBUG=*
- look at cloudformation errors
- don't sync directories: sls deploy --nos3sync 
- param indent!! 2 more spaces

## Reference

* https://www.serverless.com/framework/docs/providers/aws/guide/serverless.yml/
