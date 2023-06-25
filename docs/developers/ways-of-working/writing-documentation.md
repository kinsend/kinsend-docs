# Writing Documentation

Each aspect of the project should be documented, both in terms of functionality, as well as how code works and what
the infrastructure required to run it is.

## Github

### Repository

The code is located under the [kinsend/kinsend-docs] repository.

### Workflows

Github workflows will be triggerred on the following events:

* A push to a branch for which there is a pull request against the `master` branch.

### Commands

* To build the `mkdocs` documentations locally and serve it on [http://localhost:8000](http://localhost:8000), execute:
```
mkdocs serve
```

[kinsend/kinsend-docs]: https://github.com/kinsend/kinsend-docs
