# tf-kinsend

This repository contains the Terraform code for the infrastructure running under the `kinsend-dev` and `kinsend-prod` AWS accounts.

The repository follows `master`-based development.


## Github

### Repository

The code is located under the [kinsend/tf-kinsend] repository.

### Workflows

Github workflows will be triggerred on the following events:

* A push to a branch for which there is a pull request against the `master` branch. This will trigger the `terraform-plan` workflow.

### Commands

* To apply the Terraform changes after the plan has succeeded, post a comment under a pull request with
  the following command:
```
/apply
```

## Modules

There are copies of the modules under the [kindend/tf-kinsend] repository. 

### base-infra

This module contains base infrastructure for the root account. It contains mainly network related configuration,
such as: VPC, subnets, internet gateway, routing tables, security groups, etc.

### github-action-runners

This module contains the infrastructure for the Github Action runners. This infrastructure is running under the
AWS root account.

These GHAR-s running inside Docker containers hosted in EC2 instances

The EC2 instances are properly permissioned to allow building and managing the `kinsend-dev` and `kinsend-prod` via Terraform scripts.
Each EC2 instance is runs 2 Docker containers with the Github Action runner.

An AWS Active Scaling Group (ASG) is used to manage the EC2 instances. The ASG is currently configured to run 1 EC2 instances and can manually be increased.
During the night, the ASG is scaled down to 1 EC2 instance.

There is currently no `dev` instance for the GHAR-s.

### ecr

The ECR-s are configured in this module, as the code here is very rarely changed. This way it is possible for the
modules under the [kindend/tf-kinsend] repository to be able to do a `terraform destroy` without destroying the ECR-s.

[kinsend/tf-infrashared]: https://github.com/kinsend/tf-infrashred
[kindend/tf-kinsend]: https://github.com/kinsend/tf-kinsend
