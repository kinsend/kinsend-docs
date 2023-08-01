# Branches And Commit Messages

## Base Branches

We are basing pull requests off the following branches:

  * `master`
  * `develop`

### `master`

This is the main branch, which is (currently) used for production deployments.

### `develop`

This is the main development branch, which is used for development deployments.

### Feature Branches

All feature branches for issues raised in the same repository, you should use the following naming convention:

```
issue/${issue-number}/${issue-description}
```

For example:

```
issue/1/add-logging
```

Feature branches for issues raised in other repositories should use the following naming convention:

```
kinsend/${repositoryName}/issue/${issue-number}/${issue-description}
```

## Commit Message Style

Commits should be made using the following style:

```
kinsend/${repositoryName}#${issue-number}: Add logging

* Fixed A.
* Fixed B.
```

For example:

```
kinsend/kinsend-be#$123: Add logging

* Set up logging.
* Added more detailed logging to the `doSomething` method.
```

This will then backlink the commit to the issue in the Github repository and will be easier to track.

If the fix covers several issues, you can use the following style:

```
kinsend/${repositoryName}#${issue-number}: Add logging
kinsend/${otherRepositoryName}#${other-issue-number}: Add detailed logging for the `doSomething` method

* Set up logging.
* Added more detailed logging to the `doSomething` method.
```

## Notes

We should optimally move towards `master`-based development, where all pull requests are based off `master` branch.
This will:

  * Allow us to merge and deploy pull requests faster into the production environment, as it won't require an intermediate
    merge into the `develop` branch first and then an additional merge into the `master`.
  * Reduce the number of merge conflicts, as things would be easier to keep in sync.
  * Reduce the number of branches that need to be maintained.
  
We should instead produce versioned releases of the `master` using the commit hashes and make the deployments to the
different environments instead using these hashed versions.
