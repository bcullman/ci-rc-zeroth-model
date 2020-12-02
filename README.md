# Demo Standard Version, RC Model

See: https://github.com/conventional-changelog/standard-version

This repo is set up to demo standard version, using RC build model. 

On each merge to master, CI kicks off one addition [CI SKIP] event that does the following:

* increments the X.X.X-RC[NUM] in the package.json
* update the changelog.

PRs Merge Statements *must* be prefixed with `chore`, `docs`, `fix` or `feat`

## Cutting a release

When it is time to cut a release, run `npm run release`. This will kick off a CircleCI, that eventually leads to standard-version inspecting all previous commits since that last release, and properly incrementing the version seen in the package.json, as well as generating a release tag.