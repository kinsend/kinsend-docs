# Stripe

We're using Stripe to process payments.

## Stripe API


## Stripe-Related Dependencies


## Stripe-Related Code


## Stripe-Related Secrets

We are using the following secrets:

* `STRIPE_CURRENCY` : The currency to use for payments
* `STRIPE_PUBLISHABLE_KEY` : The publishable key
* `STRIPE_SECRET_KEY` : The secret key
* `STRIPE_STATEMENT_DESCRIPTOR` : The statement descriptor

These secrets are stored under the AWS Secret Manager under both the `kinsend-dev` and `kinsend-prod` AWS accounts and
must be kept in sync, in case you add, or update secrets.
