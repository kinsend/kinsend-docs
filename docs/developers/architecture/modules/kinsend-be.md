# kinsend-be

This module is responsible for the backend of the Kinsend application.

The code is hosted in ECS and served by an Applications Load Balancer (ALB), which also handles the SSL certificates
and serves the content over HTTPS.

## Github

### Repository

The code is located under the [kinsend/kinsend-be] repository. 

The default branch for `developers` is called `develop`. Your feature branches should be forked from the `develop`
branch and the PRs should also target the `develop` branch.

### Workflows

Github workflows will be triggerred on the following events:

* Pull request against the `master` branch (this is our `production` branch, DO NOT TARGET IT!)
* Pull request against the `develop` branch.

### PR Comment commands

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

  ```bash
npm run build
```

### Docker Image

* You can build a local image via `docker-compose build` or if you want to run in docker -- `docker-compose up`

## Testing

* To run `unit tests`:
  ```bash
  npm run test:unit
  ```
* To run `integration tests`:
  ```bash
  npm run test:integration
  ```
  This will automatically download MongoDB and run it in the background. 
  If it fails to download it means there is no [official MongoDB package](https://www.mongodb.com/try/download/community) available for your OS/distribution. 
  In that case you should install MongoDB on your system and set the binary via `MONGODB_BIN=/usr/bin/mongod`.  
    
  Here's an example for Ubuntu 23.04.
  ```bash
  MONGODB_BIN=/usr/bin/mongod npm run test:integration
  ```


* To run all tests 
  ```bash
  npm run test
  ```

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
