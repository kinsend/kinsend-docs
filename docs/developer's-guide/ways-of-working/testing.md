# Testing

## Overview

Each bit of code should have a corresponding test.

The tests should first be executed locally and then should pass in the respective checks of the pull requests.

The code in each of the repositories should be buildable using Docker.
We do not accept "works for me" as a valid excuse for not having buildable code and until code passes locally,
builds in Docker and its tests pass, it should not be merged into the base branch.

There should be:

  * Unit tests
  * Integration tests
  * End-to-end tests
  * Smoke tests

## Unit Testing

Unit tests are required for:

  * Newly added code
  * Code that has been modified to fix a bug, or issue.

Not implementing tests for either of the above, is highly discouraged, unless it's not plausible to do so.

## Integration Testing

Integrations tests should be implemented for functionality related to our third-party integrations, such as:

    * MongoDB
    * Stripe
    * Sendgrid
    * Twilio

## End-to-End Testing


## Smoke Tests

