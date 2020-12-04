# Demo Standard Version, RC Model (pre 1.0-based repo)

[![bcullman](https://circleci.com/gh/bcullman/ci-rc-zeroth-model.svg?style=svg)](https://app.circleci.com/pipelines/github/bcullman/ci-rc-zeroth-model)

This repo is set up to demo standard version

See: https://github.com/conventional-changelog/standard-version

It is also set up to demo pre 1.0-based semVer handling, meaning breaking changes are reflected by an increase in the minor version, while features, fixes, chores and docs are *ALL* represented by the patch version. (major.minor.patch).

On each merge to master, CI kicks off one addition [CI SKIP] event that does the following:

* properly increment the package.json version
* update the changelog.

PRs Merge Statements *must* be prefixed with `chore`, `docs`, `fix` or `feat`

## Cutting a release

When it is time to cut a release, run `npm run release`. This will kick off a CircleCI, that eventually leads to standard-version to increment the version seen in the package.json (my slicing off the `.RCX` value), as well as generating a release tag.