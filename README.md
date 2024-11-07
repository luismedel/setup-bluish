# setup-python

This action installs a version of Bluish making it available in the PATH.

## Basic usage

See [action.yml](https://github.com/luismedel/setup-bluish/blob/master/action.yml)

```yaml
steps:
- uses: actions/checkout@v4
- uses: actions/setup-python@v5
  with:
    python-version: '>=3.11' 
- uses: actions/setup-bluish@v2
- run: bluish --version
```

The `bluish-version` input is optional. If not supplied, the action will try to resolve the version from the default `.bluish-version` file. If the `.bluish-version` file doesn't exist the action will install the latest available Bluish version on PyPi.
