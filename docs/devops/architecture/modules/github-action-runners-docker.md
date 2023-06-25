# github-action-runners-docker

This repository produces the Docker image for the Github Action runners (GHAR-s).

The repository follows `master`-based development.

The infrastructure for the Github Action runners is Terraformed under the [kinsend/tf-infrashared] repository.
You can find the documentation for that [here](tf-infrashared.md).

## Github

### Repository

The code is located under the [kinsend/github-action-runners-docker] repository.

### Workflows

Github workflows will be triggerred on the following events:

* A push of a git tag against the `master` branch.

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

### Docker Image

The Docker image is based on [myoung34/docker-github-actions-runner] and contains a few customizations, such as packages
that we required in order to be able to run our builds using the GHAR-s.

## Testing


[myoung34/docker-github-actions-runner]: https://github.com/myoung34/docker-github-actions-runner
[kinsend/github-action-runners-docker]: https://github.com/kinsend/github-action-runners-docker
[kinsend/tf-infrashared]: https://github.com/kinsend/tf-infrashared
