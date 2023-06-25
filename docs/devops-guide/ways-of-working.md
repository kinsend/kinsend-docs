# Ways of Working

All the infrastructure should be provisioned using Terraform. There should be no manual changes to the infrastructure.

Changes should be committed via pull requests and not be done "silently" locally without the proper Github issues that
track them. 

There are certain "chicken or egg" situations in Terraform, some initial resources need to be created manually,
such as the S3 bucket for the Terraform state files, or initial users and IAM settings for them.
This is acceptable, but should be noted in the respective Github issue(s) tracking this work.

We should strive to have everything in a buildable state when we create pull requests. If at times these changes had
to be done locally and did not pass in the CI/CD for an understandable reason, but the changes passed locally,
this is acceptable, but should be noted in the respective Github issue(s) tracking this work.
