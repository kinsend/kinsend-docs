# Architecture Of The Infrastructure

Our infrastructure is hosted in AWS.

We use:

  * Github Workflows as our CI/CD
  * Terraform to provision our infrastructure
  * Docker to build and run our code
  * MongoDB as our database
  * Route53 for our DNS
  * S3 for our static assets
  * CloudFront as our CDN
  * SQS for message queues
