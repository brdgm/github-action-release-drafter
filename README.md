github-action-release-drafter
======

Create release draft based on pull requests merged since last release.

Usage example:

```yaml
name: Release Drafter

on:
  push:
    branches:
      - develop

permissions:
  contents: read

jobs:
  update_release_draft:
    permissions:
      contents: write
      pull-requests: read
    runs-on: ubuntu-latest
    steps:
      - uses: brdgm/github-action-release-drafter@main
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
```
