[![release](https://img.shields.io/github/release/DTOcean/dtocean-examples.svg)](https://github.com/DTOcean/dtocean-examples/releases/latest)

# DTOcean Examples

This repository is used for maintaining and distributing example files for
DTOcean. Archives (in zip or tar.gz formats) containing the examples can be
downloaded from the [Releases](https://github.com/DTOcean/dtocean-examples/releases/latest)
page.

The following table describes the content of each of the top level folders:

| Folder              | Description                                                                                                                                                                              |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Getting Started     | Files to accompany the [Getting Started 1: Example Project](https://dtocean.github.io/dtocean/next/user/getting_started_1.html) tutorial                                                 |
| RM3 Performance Fit | A copy of the performance fit data featured in the [DTOcean WEC Pre-processor](https://youtube.com/playlist?list=PL0_lWZCqs2h2NJWA0YX7L3_qyd2snzq_d&si=GRxgHTyom2Xi5fQi) video tutorials |
| RM3 WEC Analysis    | A copy of the WEC Analysis project featured in the [DTOcean WEC Pre-processor](https://youtube.com/playlist?list=PL0_lWZCqs2h2NJWA0YX7L3_qyd2snzq_d&si=GRxgHTyom2Xi5fQi) video tutorials |

## Contributing

Contributions are gratefully received and should be provided using pull
requests. This repository uses [dvc](https://github.com/iterative/dvc) to
manage copies of the examples which are stored on a remote service (external to
GitHub) and the repository only contains dvc managed pointers to the data.
Commands provided by dvc are used to transfer the data to and from the external
remote.

The [Poetry](https://python-poetry.org/) package manager is required to install
dvc. To collect the examples from the external service, first clone this
repository and then [install Poetry](https://python-poetry.org/docs/#installation).
From the root of the repository use Poetry to install dependencies:

```sh
poetry install
```

Now use [dvc pull](https://dvc.org/doc/command-reference/pull) to populate the
`export` folder with the database tables:

```sh
poetry run dvc pull
```

To contribute additional examples, you must set up a temporary DVC
[remote](https://dvc.org/doc/user-guide/data-management/remote-storage#remote-storage)
to share the data and make sure to check the '[Allow edits from
maintainers][allowedits]' option in the pull request. Alternatively, open an
issue to discuss other methods for transmitting the data.

## Credits

These examples are maintained by Mathew Topper at [Data Only Greater](https://www.dataonlygreater.com/).

Huge thanks is extended to the following folks for their contributions to this
collection:

- Sterling Olson at [Sandia National Labs](https://www.sandia.gov/)
- Francesco Ferri at [Aalborg University](https://www.en.aau.dk/)

## Unlicense

The examples in this repository are public domain, as detailed by the
[Unlicense](https://unlicense.org/).

[allowedits]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/allowing-changes-to-a-pull-request-branch-created-from-a-fork#enabling-repository-maintainer-permissions-on-existing-pull-requests
