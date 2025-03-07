# renovate-config-validator-action

[![License](http://img.shields.io/badge/license-mit-blue.svg?style=flat-square)](https://raw.githubusercontent.com/suzuki-shunsuke/renovate-config-validator-action/main/LICENSE) | [action.yaml](action.yaml)

`renovate-config-validator-action` is a GitHub Action for renovate-config-validator.

## How To Use

```sh
mkdir -p .github/workflows
curl -Lq -o .github/workflows/renovate-config-validator.yaml https://raw.githubusercontent.com/suzuki-shunsuke/renovate-config-validator-action/refs/heads/main/.github/workflows/renovate-config-validator.yaml
```

```yaml
---
name: renovate-config-validator
on:
  pull_request:
    paths:
      - renovate.json5
      - .github/workflows/renovate-config-validator.yaml
jobs:
  status-check:
    runs-on: ubuntu-24.04
    timeout-minutes: 10
    permissions:
      contents: read
    steps:
      - uses: suzuki-shunsuke/renovate-config-validator-action@51b62d3bf0c86d4de68c580a057c1e16f0702d07 # v0.0.1
```

## Q. What's the different from github-action-renovate-config-validator?

This action is a simple wrapper of [suzuki-shunsuke/github-action-renovate-config-validator](https://github.com/suzuki-shunsuke/github-action-renovate-config-validator).
This action is a replacement of [suzuki-shunsuke/renovate-config-validator-workflow](https://github.com/suzuki-shunsuke/renovate-config-validator-workflow).
