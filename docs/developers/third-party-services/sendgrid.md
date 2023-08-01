# SendGrid

We're using SendGrid to send e-mails.

## SendGrid API

This is the [SendGrid API](https://sendgrid.com/docs/api-reference/).

## SendGrid-Related Code

The SendGrid-related code is located under the [kinsend/kinsend-be] repository.

## SendGrid-Related Secrets

We are using the following secrets:

* `SEND_GRID_API_KEY` : This is the SendGrid API key used to send e-mails

These secrets are stored under the AWS Secret Manager under both the `kinsend-dev` and `kinsend-prod` AWS accounts and
must be kept in sync, in case you add, or update secrets.
