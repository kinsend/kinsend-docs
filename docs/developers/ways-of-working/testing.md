# Testing

## Overview

Test cases are an essential part of the development process. They ensure the end product works as expected and 
mitigate future changes from introducing regressions that could affect the stability of the platform. For this reason 
writing tests across all Kinsend repositories should be considered mandatory, because:

!!! bug "A code that cannot be tested or is not covered by test cases is flawed code."

It is  **your responsibility**, as the developer, to write **sufficient test cases** for the feature(s) you are implementing. 
In addition, when you are fixing a bug or a corner case you **should** also include a test case that reproduces
the bug/corner case and validates it has been fixed.

## Thought process

When you write test cases you should follow these key principles:

1. Have a clear understanding of the feature specs - what is this feature about and what does it do?
2. How is it supposed to be used? (i.e. an  `API function` that is shared across the project; a `react component` that is reusable; etc)
3. Think of the basic use cases and how to cover them in the test case:
   1. What kind of `input` combination(s) is this piece of code expected to receive? 
   2. What is the expected `output` based on the received `input` ?
4. Written tests should be locally runnable, and then should pass in the respective checks inside the pull request.

The above principles are very simple and should help you produce high quality test cases.
We are aiming at having at minimum 80% of the code lines covered by test cases.

In a perfect world we would have 100% code coverage. Unfortunately there are always some "gray areas" that cannot be 
fully tested or might not need to be. If the task you are working on is one of those cases -- you should
alert us and leave the necessary comments in the code and PR.

## Types of tests

### Unit Testing (UT)

Unit tests are used to test small portions of isolated code that are not coupled with anything or the very lightly 
coupled in a way that allows for easy mocking. Whenever a choice between `Unit Test` and  `Integration Test` is possible, 
you should always aim at implementing the `Unit Tests`. The reason for this is simply because `Unit Tests` run significantly
faster due to the fact they do not require additional resources such as Database, Stripe, Twilio, etc in order to 
execute and test the code. 

A perfect candidate for a `Unit Test` would be a helper function such as `phoneSanitizer(phone: string)` that 
accepts a `phone number` which needs to be sanitized. Let's assume the specs for this function are:

1. Phone number needs to be converted from a `string` into a `number`
2. As this will be converted into a `number` -- we need to remove any formatting such as `+1`, white space (` `), 
   dashes `-`, or brackets `()`. 

You don't really need to have a fully configured NestJS application containing every possible DI configuration, 
a running MongoDB, Stripe and Twilio in order to test this function. 

### Integration Testing (IT)

Integration tests are used to test more complicated code implementations that require additional resources in order
to execute. Good candidates for `Integration Tests` are features that interact with MongoDB, Stripe and Twilio.

Let's assume you have a `webhook` that Twilio is going to send a payload to whenever an SMS message has been received 
from a customer. The specs for this functionality are:

1. Webhook receives the SMS message
2. Processes it
3. Sanitizes the payload and transforms it into a DTO
4. Saves the DTO into the correct `message thread` that corresponds to the client <=> customer interaction. 

Since a database is involved you can't really write this as a `Unit Test`, because you need to ensure the 
received payload has been properly processed and actually **stored** into the database. As you will be processing 
and **transforming** the received SMS payload you should write a `Unit Test` for the function that will be doing the 
payload transformation as that will catch problems early in the testing cycle and spare you time waiting for `Integration Tests` 
to complete and catch the problem.

### End-to-End Testing (e2e)

End-to-End tests are usually testing if range of features works from the user’s perspective.
In most cases these tests are in the Frontend and ensure that the UI behaves as expected based on specific events
or user flows. 

