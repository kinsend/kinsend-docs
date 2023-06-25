# kinsend-fe

This module is responsible for the frontend of the Kinsend application.

The code is hosted in S3 and served by CloudFront.

## Github

### Repository

The code is located under the [kinsend/kinsend-fe] repository.

### Workflows

Github workflows will be triggerred on the following events:

* Pull request against the `master` branch.
* Pull request against the `develop` branch.

### Commands

* To build and push the code to S3, post a comment under a pull request with the following command:
```
/s3:push
```

## Building

### Code

### Docker Image

## Testing

## Environment Details

### Development

The development environment is based on the code in the `develop` branch.

In AWS, the development environment is called `kinsend-dev`.

The Docker repository for the development environment is called `kinsend-fe`.

The URL for the development environment is [https://app.dev.kinsend.io](https://app.dev.kinsend.io).

### Production

The production environment is based on the code in the `master` branch.

In AWS, the production environment is called `kinsend-prod`.

The Docker repository for the production environment is called `kinsend-fe`.

The URL for the production environment is [https://app.kinsend.io](https://app.kinsend.io).

[kinsend/kinsend-fe]: https://github.com/kinsend/kinsend-fe
