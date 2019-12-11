# CFN Custom Resource Manager demo
* Fork the github repo: https://github.com/tonyfruzza/aws_cfn_cust_res_mgr_demo into your own git account.
* Modify the icon list to the custom list provided through direct message
* Launch the runway project in your lab account make the necessary modifications to have a unique S3 bucket for web hosting.
* Once launched update the static html file to point to your newly launched API GW end point.
* Be prepared answer the questions in a direct message before the due date

### Questions
1. What is the URL to your forked git repo of the project?
  * https://github.com/gh-dominick/aws_cfn_cust_res_mgr_demo
2. What is the URL to your web hosted static S3 bucket?
  * http://display-api-dev-dnguyen-static-site.s3-website-us-west-2.amazonaws.com
3. What is your web hosted static s3 bucket policy?
  * {
      "Version": "2008-10-17",
      "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::display-api-dev-dnguyen-static-site/*"
        }
      ]
    }
4. What is the github URL to the serverless framework plugin that was used to upload the static s3 content?
  * https://github.com/k1LoW/serverless-s3-sync
5. What is the name of the lambda function launched for managing the custom cloudformation resources?
  * cfn-res-mgr-demo-lookup
6. What is the name of the table that the state of the resources are stored in?
  * cfn-res-mgr-dev-state
7. Which javascript library is used to draw the icons?
  * paper.js
8. Which headers need to be present from the API server to allow for CORS?
  * 'Access-Control-Allow-Origin': '*'
9. What common ID type is used for the physical resource ID?
  * 32 hexidecimal UUID
10. Do custom resource lambda functions require IAM permissions to interact with cloudformation (not including the IAM managed role permission in AWSLambdaBasicExecutionRole)?
  * No
