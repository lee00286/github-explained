# Useful Github Actions

## Table of Contents

1. [Actions for Automation](#actions-for-automation)

---

## Actions for Automation

* [Auto-Add Contributors](#auto-add-contributors)
* [Labeler](#labeler)

### Auto-Add Contributors

[Auto-Add Contributors](https://github.com/marketplace/actions/auto-add-contributors) allows you to automatically add contributors of your open-source project to your markdown file.

1. Create a `.github/workflows/contributors.yml` file.
1. Copy and paste the lines below in the file you just created. Replace `OWNER-NAME` and `REPO-NAME` on your need.

:memo: Code blocks below are for different needs, so choose the right version of code.

:memo: The workflow will not be triggered if `CONTRIBUTOR` includes emoji. For example, if you set `CONTRIBUTOR` as `## Contributors`, then `## Contributors :sparkles:` won't work.

**Updates contributors at the scheduled time**

```
name: Add contributors
on:
  schedule:
    - cron:  '20 20 * * *'

jobs:
  add-contributors:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - uses: BobAnkh/add-contributors@master
      with:
        REPO_NAME: 'OWNER-NAME/REPO-NAME'
        CONTRIBUTOR: '## Contributors'
        COLUMN_PER_ROW: '6'
        ACCESS_TOKEN: ${{secrets.GITHUB_TOKEN}}
        IMG_WIDTH: '100'
        FONT_SIZE: '14'
        PATH: '/README.md'
        COMMIT_MESSAGE: 'docs(README): update contributors'
        AVATAR_SHAPE: 'round'
```

**Updates contributors when someone requests for the pull request**

```
name: Add contributors
push:
  branches:
    - master

jobs:
  add-contributors:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - uses: BobAnkh/add-contributors@master
      with:
        REPO_NAME: 'OWNER-NAME/REPO-NAME'
        CONTRIBUTOR: '## Contributors'
        COLUMN_PER_ROW: '6'
        ACCESS_TOKEN: ${{secrets.GITHUB_TOKEN}}
        IMG_WIDTH: '100'
        FONT_SIZE: '14'
        PATH: '/README.md'
        COMMIT_MESSAGE: 'docs(README): update contributors'
        AVATAR_SHAPE: 'round'
```

### Labeler

[Labeler](https://github.com/marketplace/actions/labeler) allows you to automatically label pull requests.

1. Create a `.github/labeler.yml` file. Follow the explanation on Marketplace and include a list of labels and [minimatch](https://github.com/isaacs/minimatch) globs
1. Create a `.github/workflows/labeler.yml` file.
1. Copy and paste the lines below in the file you just created.

```
name: "Pull Request Labeler"
on:
- pull_request_target

jobs:
  triage:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/labeler@main
      with:
        repo-token: "${{ secrets.GITHUB_TOKEN }}"
```
