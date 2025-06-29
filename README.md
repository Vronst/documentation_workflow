# Documentation Workflow

This repository contains reusable GitHub Actions workflows for consistent automation across multiple projects.

## 🔁 Reusable Release Workflow

### Usage

*Requirements:*
- directory colled doc
- sphinx generated documentation (shpinx-apidoc)

```yaml
# Exapmle job
name: test

on:
  push:
    branches:
      - main

# needed permissions
permissions:
  contents: write
  packages: write

# This is most important part
# This uses release workflow
jobs:
  release:
    uses: Vronst/documentation_workflow/.github/workflows/doc_workflow.yml@1.0.0
    with:
      python-version: '3.13'
```
