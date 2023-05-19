# github-workflows
Repository for shared GitHub Action workflows.

[GitHub documentation](https://docs.github.com/en/actions/using-workflows/reusing-workflows).

## Workflows

### `platformio-build.yaml`
Build [PlatformIO](https://platformio.org/) project and optionally upload firmware artefacts.

```yaml
jobs:
  call-platformio-build:
    uses: ravngr/github-workflows/.github/workflows/platformio-build.yaml@main
    with:
      pio-environment: <environment>
      upload-firmware: false
```

### `pre-commit.yaml`
Runs [pre-commit](https://pre-commit.com/) against repository files.

```yaml
jobs:
  call-pre-commit:
    uses: ravngr/github-workflows/.github/workflows/pre-commit.yaml@main
```

### `submodule-update.yaml`
Checks out repoisitory and updated submodules. When changes are found a PR is opened using [peter-evans/create-pull-request](https://github.com/peter-evans/create-pull-request). Requires additional permissions to create PR.

```yaml
permissions:
  pull-requests: write
  contents: write

jobs:
  call-submodule-update:
    uses: ravngr/github-workflows/.github/workflows/submodule-update.yaml@main
```

### `yamllint.yaml`
Runs [yamllint](https://www.yamllint.com/) against repository files.

```yaml
jobs:
  call-yamllint:
    uses: ravngr/github-workflows/.github/workflows/yamllint.yaml@main
```
