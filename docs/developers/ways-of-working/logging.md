# Logging


## Logging Library Used


## Logging levels

The logging levels are:

* `DEBUG` : This level is typically used for detailed information useful for debugging and troubleshooting. 
  It's the lowest severity level and provides the most detailed logs. Debug messages are usually only needed during
  development or when investigating specific issues.
  This level should only be used for debugging purposes for local development, or in the `dev` environment.
  It should not be used in production.

* `INFO` : This level is used to convey general information about the progress or status of an application.
  It's useful to log important events or milestones that can help understand the flow of the program. Info messages are
  often used for tracking the overall execution and to provide context.

* `WARNING` : Warnings are used to indicate potential issues or unusual conditions that may not necessarily cause an
  error but could lead to problems if ignored. For example, deprecated functions or configuration settings that are not
  optimal. Warnings serve as a heads-up to developers or administrators that something might need attention.

* `ERROR`: The `ERROR` level is used to log errors or exceptional conditions that should be addressed. It indicates that
  something has gone wrong, but the application can still continue to run. Errors might include failed operations,
  incorrect input, or resource unavailability. Error messages help identify problems that need attention but don't
  necessarily halt the execution.

* `CRITICAL`: This level is used to log serious errors that can potentially cause application failure or lead to
  data loss. These are severe issues that require immediate attention. Critical messages may include unexpected
  exceptions, system failures, or unrecoverable errors. They indicate a severe state that requires intervention.

* `FATAL`: The FATAL level is often used interchangeably with CRITICAL and represents the highest severity level.
  It signifies errors that are so critical that they cause the application to terminate or result in a complete system
  failure. Fatal errors usually indicate a severe problem that cannot be recovered from and require
  immediate investigation.

## AWS CloudWatch Logs

We are collecting all the logs for the [kinsend-be](https://github.com/kinsend/kinsend-be) to Cloudwatch, as the
application is running as Docker containers in ECS.
