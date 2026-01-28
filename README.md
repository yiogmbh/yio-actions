# yio-actions

This repository contains several templates that might be useful to create build pipelines with ease.

> **Attention** The actions provided will work with a special runner image only
> which is based on the official gitea runner image.

## Actions

### python

#### uv-xxx

A bunch of useful actions to deal with uv as python package manager

- `uv-build`: Build the given project/package
- `uv-login`: Use the uv cli to login to private package registries
- `uv-publish`: Use uv to publish a package to private registries
- `uv-publish-legacy`: legacy version
- `uv-tox`: Use uv and tox to run tests, linters ...

### version

A bunch of composite actions to handle versioning based on 
[gitversion (v5)](https://gitversion.net/5.12.0/docs/).

- `version-info`: Outputs the version information as JSON and some
  outputs for further processing.

  Outputs

- `version-tag`: Can create a tag within the repository based on given version inputs.
- `version-release`: Creates a release within the repository (including tag).

- `version-bump`: Bumps the version based on the given input.

## Runner Image requirements

The runner image must have the following tools installed:

- [`gitversion`](https://gitversion.net/5.12.0/docs/)
- [`jq`](https://stedolan.github.io/jq/)
- [`dasel`]()
- [`tox`]() (incl. `tox-uv`)
- [`uv`](https://astral.sh/uv) (incl. `keyring support`)
- [`bump-my-version`](https://callowayproject.github.io/bump-my-version/)
