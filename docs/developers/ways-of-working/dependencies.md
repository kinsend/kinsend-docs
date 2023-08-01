# Dependencies

Kinsend.io is based on Open Source software and uses a number of dependencies.
These dependencies are managed using `npm` and are listed in the `package.json` files of the respective repositories.

We should aim to keep these dependencies up-to-date and to fix any identified vulnerabilities with priority.

## List of Dependencies


## Vulnerabilities in Dependencies

Vulnerabilities in dependencies should be tracked and fixed as soon as possible.

When you build the code using `npm install`, the `npm audit` command will be run automatically and will report
any vulnerabilities it finds. You can also run `npm audit` manually at any time.

If your changes introduce new vulnerabilities, you will see a warning when you run `npm install`:

```
found 1 vulnerability (1 low) in 1 scanned package
  1 vulnerability requires manual review. See the full report for details.
```

You can then run `npm audit` to see the details of the vulnerability and how to fix it.

## Dependency Updates Via @dependabot

We use [Dependabot](https://dependabot.com/) to automatically update dependencies. Dependabot will create a pull request
with the updated dependency and will run the tests.

If such automated pull requests are created and look good, they should be reviewed and merged as soon as possible,
as we don't want to accumulate technical debt for this.
