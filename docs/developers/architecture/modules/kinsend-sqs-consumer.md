# kinsend-sqs-consumer

This module is responsible for the handling messages sent to the SQS message queue of the Kinsend application.

## Github

### Repository

The code is located under the [kinsend/kinsend-sqs-consumer] repository.

### Workflows

Github workflows will be triggerred on the following events:

* Pull request against the `master` branch.
* Pull request against the `develop` branch.

### Commands

* To publish a new Docker image to the ECR, post a comment under a pull request with the following command:
```
/docker:push
```

* To build and deploy the code to EC2, post a comment under a pull request with the following command:
```
/ec2:deploy
```

## Building

### Code

### Docker Image

## Testing

## Environment Details

### Development

The development environment is based on the code in the `develop` branch.

In AWS, the development environment is called `kinsend-dev`.

The Docker repository for the development environment is called `kinsend-sqs-consumer`.

### Production

The production environment is based on the code in the `master` branch.

In AWS, the production environment is called `kinsend-prod`.

The Docker repository for the production environment is called `kinsend-sqs-consumer`.

[kinsend/kinsend-sqs-consumer]: https://github.com/kinsend/kinsend-sqs-consumer
