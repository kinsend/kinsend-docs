# AWS

We're using AWS to host our infrastructure.

Our infrastructure is split into two AWS accounts that provide a separation between the development and
production environments:

* `kinsend-dev`
* `kinsend-prod`

## Services Used

* EC2 : Used for running the [kinsend/kinsend-sqs-consumer] and for hosting the Github Action Runners
* Certificate Manager : Used for managing SSL certificates
* CloudFront : Used for serving the [kinsend/kinsend-fe] and content from the S3 buckets
* CloudWatch : Used for logging
* ECR : Used for storing Docker images
* ECS : Used for running the [kinsend/kinsend-be] services
* IAM : Used for controlling access to AWS resources
* Route53 : Used for our DNS records
* Secrets Manager : Used for storing secrets
* S3 : Used for static website hosting, including user resources
* SQS : Used by the [kinsend/kinsend-sqs-consumer] to queue and process SMS messages   
* VPC : Used for management of network resources

[kinsend/kinsend-be]: https://github.com/kinsend/kinsend-be
[kinsend/kinsend-fe]: https://github.com/kinsend/kinsend-fe
[kinsend/kinsend-sqs-consumer]: https://github.com/kinsend/kinsend-sqs-consumer
