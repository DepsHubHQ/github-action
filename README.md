# DepsHub Github Action

Use this action to run DepsHub on your repository.

## Example

```yaml
name: Run DepsHub

on:
  push:
    branches:
      - main
  pull_request:

jobs:
  depshub-lint:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Run DepsHub
        uses: DepsHubHQ/depshub-action@v1
        with:
          path: './src'                    # optional
          config: './depshub-config.yml'   # optional
```


## Inputs

- `path` - The path to the directory containing the dependencies. Default is `./`.
- `config` - The path to the DepsHub configuration file. Default is `./depshub-config.yml`.

See the [documentation](https://docs.depshub.com/guides/integrations/) for more information.
