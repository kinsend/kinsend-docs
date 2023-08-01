# Secrets Management

Secrets are sensitive information that should not be publicly available. Examples of secrets include:
* API keys
* Credentials (usernames, passwords, etc.)
* Private keys (SSH, GPG, etc.)
* Certificates (SSL, TLS, etc.)
* Tokens
* Any other confidential information used to access a protected resource or system

Such information should not be committed to version control.

## AWS Secrets Manager

We store all of our secrets in the AWS Secrets Manager. This allows us to:

* Store, manage, and retrieve secrets throughout their lifecycle
* Rotate secrets safely
* Control access to secrets
* Audit secret usage
* Integrate with other AWS services
* Integrate with CI/CD pipelines

There is a set of secrets per environment (for `dev` and `prod`).

### Naming Conventions For Secrets In The Secrets Manager

For the `dev` environment, the naming convention is:
* `dev/var/${VAR_NAME}`: For variables

For the `prod` environment, the naming convention is:
* `prod/var/${VAR_NAME}`: For variables

## Local Secrets Management (`.env` files)

We use `.env` files to store secrets locally. These files should not be committed to the repository, as they contain
sensitive information. They should be used only for local development and testing purposes.

## Git

Every measure should be made to __*NOT*__ commit secrets to Git. This includes:

* `.env` files
* Key files
* Certificates files
* Storing of variables with hard-coded values in the code that represent secrets

If you accidentally commit secrets to Git, you should:

* Immediately rotate them
* If this was committed to a feature branch and re-writing the history is not a problem, you should:
  * Re-write the history of the feature branch to remove the secrets
  * Force push the branch to the remote repository

### GitGuardian

We have set up [GitGuardian](https://gitguardian.com/) to scan our repositories for secrets.

GitGuardian can:

* Scan the entire repository's history for secrets
* Scan pull requests for secrets

If a secret is found to be leaked, GitGuardian will:

* Notify us via e-mail
* Notify us via Slack
* Add a comment to the respective pull request, if this was identified in a pull request
* Add an issue for this in the GitGuardian web UI

Access to GitGuardian can be provided by the DevOps team.

### Github Secrets

Github Secrets are used to store secrets that will be used by the CI/CD pipelines. Secrets defined here should only be
related to build and deploying code, as these pipelines already have access to the AWS Secret Manager and can retrieve
and embed secrets from there.

Secrets defined in the Github Secrets should not relate to the application itself.
