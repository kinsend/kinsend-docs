# MongoDB

We're using the cloud-based MongoDB offering as our database.

## MongoDB API


## MongoDB-Related Dependencies


## MongoDB-Related Code


## MongoDB-Related Secrets

We are using the following secrets:

* `MONGODB_DATABASE` : The name of the database
* `MONGODB_URI` : The URI to use to establish the connection
* `MONGODB_USERNAME` : The username to use to establish the connection
* `MONGODB_PASSWORD` : The password to use to establish the connection

These secrets are stored under the AWS Secret Manager under both the `kinsend-dev` and `kinsend-prod` AWS accounts and
must be kept in sync, in case you add, or update secrets.
