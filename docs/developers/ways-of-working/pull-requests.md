# Pull Requests

Pull requests should be based against the `master` or `develop` branches.

It should be a rare exception for a pull request to not have an actual issue associated with it.

Feature branches should not be based on each other, they should only be based on the `master` or `develop` branches.

A feature branch should try to contain the changes only to its associate issue. If a feature branch contains a large
number of changes across multiple issues, it should be split into multiple feature branches. Of course, while
sometimes this is not possible, having too many changes spanning across various functionality makes it harder to review
the pull request and assess the impact of the changes which can lead to both a longer development and review process.
We should try to avoid this, so that we can would be possible to have quicker development and review cycles,
leading to quicker deployments

## Commit Messages

Commit messages should contain the issue number, such as for example `kinsend/kinsend-be#123`,
where `kinsend/kinsend-be` is the name of the repository in which the issue was raised and `#123` is the number
of the issue. This will backlink the commit to the issue and will make it easier to track the changes directly from the
Github issue.

Commit messages should be in the following format:

```
kinsend/kinsend-be#123: Implement support for some cool feature

* Add support for ABC in the UI.
```

If the pull request contains more changes, feel free to list them out in the commit message.

* If a change relates to multiple issues in the same repository, you can list them out in the commit message like this:
```
kinsend/kinsend-be#123: Implement support for some cool feature

* Add support for ABC in the UI.

kinsend/kinsend-be#551: Implement support for some other feature

* Fixed the issue with the pop-up.
* Change the color of the button.
```

* If a change relates to multiple issues in the same repository, you can list them out in the commit message like this:
```
kinsend/kinsend-be#123: Implement support for some cool feature

* Add support for ABC in the UI.

kinsend/kinsend-be#551: Implement support for some other feature

* Fixed the issue with the pop-up.
* Change the color of the button.
```

* If a change relates to multiple issues in different repositories, you can list them out in the commit message like this:
```
kinsend/kinsend-be#123: Implement support for some cool feature

* Add support for ABC in the UI.

kinsend/kinsend-fe#551: Implement support for some other feature

* Fixed the issue with the pop-up.
* Change the color of the button.
```

## Github Checks

All Github checks should pass before a pull request can is merged.

Branches of pull requests must be rebased against their base branch before they are merged.
