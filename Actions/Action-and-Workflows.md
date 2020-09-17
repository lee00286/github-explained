# Action and Workflows

## Table of Contents

1. [What is an Action](#what-is-an-action)
1. [How to Begin](#how-to-begin)
1. [How to Build an Workflow](#how-to-build-an-workflow)
1. [How to Run a Workflow Manually](#how-to-run-a-workflow-manually)

---

## What is an Action

[GitHub Action](https://docs.github.com/en/actions/getting-started-with-github-actions/about-github-actions) allows you to create and automate SDLC workflows in your repository.

Various actions can be combined to create a custom workflow. Workflow is custom automated process that you can set up in your repository.

GitHub Actions allows you to build end-to-end CI and CD capabilities in your repository. CI([Continuous Integration](https://docs.github.com/en/actions/building-and-testing-code-with-continuous-integration/about-continuous-integration)) is a software practice that should be commited to a shared repository frequently.

---

## How to Begin

If none of the workflows is added to your repository, you might want to use workflow templates.

### Add a Workflow File

Create a directory called `.github/workflows` at the root of your repository. In the directory, add a `.yml` or `.yaml` file. For example, `.github/workflows/contribution.yml`.

After the file is created, customize the file to create your workflow.

### Add a Workflow Template

Navigate to **Actions** category in your repository. Then, you will see the message:

> Get started with GitHub Actions

Below the message, you would see various suggested or popular workflows listed. If there's any template you'd like to use, then click **Set up this workflow** under the name of the template.

If you want to use your own workflow, then click **set up a workflow yourself**. Then, you will be able to use GitHub Action through stored workflows in `.github/workflows` directory.

### [Use GitHub Marketplace](https://docs.github.com/en/actions/getting-started-with-github-actions/using-actions-from-github-marketplace)

[GitHub Marketplace](https://github.com/marketplace?type=actions) is a webpage where you can find actions created by the GitHub community. You can find some useful actions [here](/Actions/Useful-Actions.md).

There are two ways of using GitHub Marketplace:
1. [Use Workflow Editor](#use-workflow-editor)
1. [Browse in GitHub Marketplace](#browse-in-github-marketplace)

#### Use Workflow Editor

Browse to the workflow file in your repository. When you open the workflow editor, Github Marketplace sidebar will be shown to the right of the editor. Click the Action you want to use and follow the instruction inside. If you don't know how to follow the instruction, read [Browse in GitHub Marketplace](#browse-in-github-marketplace).

#### Browse in Github Marketplace

[Create the workflow file](#add-a-workflow-file). Navigate to the action you want to use. Copy the workflow syntax under **Installation** and paste in your workflow. 

If there are more variables to provide, set them in your workflow.

---

## How to Build an Workflow

### [Workflow Syntax](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions)

### [Trigger a Workflow with Events](https://docs.github.com/en/actions/configuring-and-managing-workflows/configuring-a-workflow#triggering-a-workflow-with-events)

There are three ways to configure a workflow:

* [Event on GitHub Occurs (commit, pull request, issue)](#event-on-github-occurs)
* [Scheduled Event Begins](#scheduled-event-begins)
* External Event Occurs

Use `name:` to add an event value after the workflow name and use `on:` to trigger a workflow after an event. Below is the example of using these syntax.

```
name: WORKFLOW-NAME
on: EVENT
```

#### Event on GitHub Occurs

You can trigger the action through pull request. Below is an example of triggering workflow after pushing to the master branch.

```
on:
  push:
    branches:
      - master
```

#### Scheduled Event Begins

POSIX cron syntax allows you to schedule a workflow. Use `schedule:` to schedule a workflow, and `cron: '* * * * *'` to set the time when you want to trigger a workflow.

Each star represents:

1. Minute [0, 59]
1. Hour [0, 23]
1. Day of the month [1, 31]
1. Month of the year [1, 12]
1. Day of the week [0, 6] (0 is Sunday)

Cron follows STC (System Time Clock). [Crontab Guru](https://crontab.guru/#20_20_*_*_*) will help you to easily edit cron schedule expression.

Below is an example of using schedule and cron syntax.

```
on:
  schedule:
    cron:  '20 20 * * *'
```

## How to Run a Workflow Manually

* [Workflow Dispatch](#workflow-dispatch)
* [Trigger the Workflow Dispatch](#trigger-the-workflow-dispatch)

### Workflow Dispatch

[Run a Workflow Manually](https://docs.github.com/en/actions/configuring-and-managing-workflows/configuring-a-workflow#manually-running-a-workflow)

Configuring workflow allows you to run a workflow manually. Place `workflow_dispatch` inside `on:` syntax to use it. Below is an example of the manual workflow using [Ubuntu](https://ubuntu.com/). If `name` is provided, then 'SUCCEED' is printed. If it isn't provided, 'FAILED' is printed instead.

```
name: Manually triggered workflow
on:
  workflow_dispatch:
    inputs:
      name:
        description: 'SUCCEED'
        required: true
        default: 'FAILED'
      home:
        description: 'location'
        required: false

jobs:
  say_hello:
    runs-on: ubuntu-latest
    steps:
    - run: |
        echo "Hello ${{ github.event.inputs.name }}!"
        echo "- in ${{ github.event.inputs.home }}!"
```

### Trigger the Workflow Dispatch

Triggering the `worfklow_dispatch` event allows you to run the workflow manually. You can trigger it from the Actions tab.

On GitHub webpage, navigate to the **Actions** tab. If you haven't use Actions in the repository yet, then read [Add a Workflow Template](#add-a-workflow-template) section.

Click the workflow you want to run in the left sidebar. In the workflow, there will be a list of workflow runs. Select **Run workflow** and select the branch where the workflow will run and type the input parameters. Then, click **Run workflow** button.
