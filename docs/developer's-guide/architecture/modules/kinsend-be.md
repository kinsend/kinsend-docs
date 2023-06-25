# kinsend-be

This module is responsible for the backend of the Kinsend application.

The code is hosted in ECS and served by an Applications Load Balancer (ALB), which also handles the SSL certificates
and serves the content over HTTPS.

## Github

### Repository

The code is located under the [kinsend/kinsend-be] repository.

### Workflows

Github workflows will be triggerred on the following events:

* Pull request against the `master` branch.
* Pull request against the `develop` branch.

### Commands

* To publish a new Docker image to the ECR, post a comment under a pull request with the following command:
```
/docker:push
```

* To build and deploy the Docker image to ECS, post a comment under a pull request with the following command:
```
/ecs:deploy
```

## Building

### Code

### Docker Image

## Testing

## Environment Details

### Development

The development environment is based on the code in the `develop` branch.

In AWS, the development environment is called `kinsend-dev`.

The Docker repository for the development environment is called `kinsend-be`.

The container is using the `kinsend-be-task-ecs-logs` CloudWatch log group for logging.

The URL for the development environment is [https://api.dev.kinsend.io](https://api.dev.kinsend.io).

### Production

The production environment is based on the code in the `master` branch.

In AWS, the production environment is called `kinsend-prod`.

The Docker repository for the production environment is called `kinsend-be`.

The container is using the `kinsend-be-task-ecs-logs` CloudWatch log group for logging.

The URL for the production environment is [https://api.kinsend.io](https://api.kinsend.io).

[kinsend/kinsend-be]: https://github.com/kinsend/kinsend-be
