# Other Publications

[![exist-db CI](https://github.com/HistoryAtState/other-publications/actions/workflows/build.yml/badge.svg)](https://github.com/HistoryAtState/other-publications/actions/workflows/build.yml)

Source data for:

- [Foreign Relations of the United States Guide to Sources on Vietnam, 1969-1975](https://history.state.gov/historicaldocuments/guide-to-sources-on-vietnam-1969-1975)
- [Office of the Historian Frequently Asked Questions](https://history.state.gov/about/faq)
- [Homes of the Department of State, 1774-1976](https://history.state.gov/departmenthistory/buildings)
- [Short History of the Department of State](https://history.state.gov/departmenthistory/short-history)
- [U.S. Foreign Relations Materials in the Pre-1861 U.S. Congressional Serial Set](https://history.state.gov/historicaldocuments/pre-1861/serial-set)
- [Views From the Embassy: The Role of the U.S. Diplomatic Community in France, 1914](https://history.state.gov/departmenthistory/wwi)

## Build

1. Single `xar` file: The `collection.xconf` will only contain the index, not any triggers!

    ```shell
    ant
    ```

    1. Since Releases have been automated when building locally you might want to supply your own version number (e.g. `X.X.X`) like this:

    ```shell
    ant -Dapp.version=X.X.X
    ```

    During a release the property `-Drelease=true` must be set for proper processing of template files.

## Release

Releases for this data package are automated. Any commit to the `master` branch will trigger the release automation.

All commit message must conform to [Conventional Commit Messages](https://www.conventionalcommits.org/en/v1.0.0/) to determine semantic versioning of releases, please adhere to these conventions, like so:

| Commit message  | Release type |
|-----------------|--------------|
| `fix(pencil): stop graphite breaking when too much pressure applied` | Patch Release |
| `feat(pencil): add 'graphiteWidth' option` | ~~Minor~~ Feature Release |
| `perf(pencil): remove graphiteWidth option`<br/><br/>`BREAKING CHANGE: The graphiteWidth option has been removed.`<br/>`The default graphite width of 10mm is always used for performance reasons.` | ~~Major~~ Breaking Release |

When opening PRs commit messages are checked using commitlint.