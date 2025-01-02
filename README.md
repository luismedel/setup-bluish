# setup-bluish

This action installs a version of [Bluish](https://github.com/luismedel/bluish) making it available in the PATH.

## Usage

See [action.yml](https://github.com/luismedel/setup-bluish/blob/master/action.yaml)

```yaml
steps:
- uses: actions/checkout@v4
- uses: luismedel/setup-bluish@v3
- run: |
    bluish --version
```

The `bluish-version` input is optional. If not supplied, the action will try to resolve the version from the default `.bluish-version` file. If the `.bluish-version` file doesn't exist the action will install the latest available Bluish version on PyPi.
