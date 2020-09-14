# Action and Workflows

## Table of Contents

1. [What is an Action](#what-is-an-action)
1. [How to Begin](#how-to-begin)
1. [How to Build an Workflow](#how-to-build-an-workflow)

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

### [Workflow Syntax](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobsjob_idsteps)

### [Trigger a Workflow with Events](https://docs.github.com/en/actions/configuring-and-managing-workflows/configuring-a-workflow#triggering-a-workflow-with-events)

There are three ways to configure a workflow:

* Event on GitHub occurs (commit, pull request, issue)
* Scheduled event begins
* External event occurs
