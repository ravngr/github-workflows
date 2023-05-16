# github-workflows
Repository for shared GitHub Action workflows.

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

### `yamllint.yaml`
Runs [yamllint](https://www.yamllint.com/) against repository files.

```yaml
jobs:
  call-yamllint:
    uses: ravngr/github-workflows/.github/workflows/yamllint.yaml@main
```
