# Fork and Contribute

## Table of Contents
- [Requirement Before the Contribution](#requiurement-before-the-contribution)
- [How to Begin](#how-to-begin)
- [How to Build Local Project](#how-to-build-local-project)
- [How to Contribute](#how-to-contribute)

## Requirement Before the Contribution

Before you to contribute to an open-source project, please read through readme, contribution, and code of conduct files, if available. They will help you to learn how to install the file, how to contribute, and how to hold a respectful and harassment-free space for all project participants.

## How to Begin

Before contributing to an open-source project on GitHub, you'll need to [set up Git](https://docs.github.com/en/github/getting-started-with-github/set-up-git).

### Fork the Repository

[Forking a repository](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) allows you to freely experiment with changes without affecting any of the original code.

Click **Fork** (in the top-right corner of the page) to copy this repository to your GitHub account.

### Clone the Fork

[Creating a local clone of your fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo#step-2-create-a-local-clone-of-your-fork) lets you save the files in that repository on your computer.

Use `git` to clone the fork. Make sure to replace `YOUR-USERNAME` with your GitHub username and `REPOSITORY-NAME` with the repository name.

```
$ git clone https://github.com/YOUR-USERNAME/REPOSITORY-NAME
```

### Create the Branch

[Creating a Branch](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-and-deleting-branches-within-your-repository) allows you to isolate edits without affecting the other branches in the repository.

Create a branch with your username and [Issue ID](https://github.com/lee00286/github-explained/issues). Don't forget to replace `YOUR-USERNAME` and `ISSUE-TITLE-ISSUEID`.

```
$ git checkout -b YOUR-USERNAME/ISSUE-TITLE-ISSUEID
```

For example,

```
$ git checkout -b lee00286/improve-contribution-file-1234
```

## How to Build Local Project

### Creating a Local Clone

[Creating a Local Clone](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo#step-2-create-a-local-clone-of-your-fork) allows you to get a copy of the project running locally on your computer.

Copy the web URL of your forked repository, which will be look like `https://github.com/YOUR-USERNAME/REPOSITORY-NAME`.

Then, open Terminal and move to the location where you want the cloned directory. Then, type `git clone` and paste the copied URL. Don't forget to replace `YOUR-USERNAME` and `REPOSITORY-NAME`.

```
$ git clone https://github.com/YOUR-USERNAME/REPOSITORY-NAME
```

When you press enter, then the progress will be shown like the lines below, and your local clone will be created.

```
$ git clone https://github.com/YOUR-USERNAME/REPOSITORY-NAME
> Cloning into `REPOSITORY-NAME`...
> remote: Counting objects: 10, done.
> remote: Compressing objects: 100% (8/8), done.
> remove: Total 10 (delta 1), reused 10 (delta 1)
> Unpacking objects: 100% (10/10), done.
```

## How to Contribute

You are now ready for the contribution! Feel free to make changes in your fork of this project.

### Submit a Pull Request

After you've made any changes, you need to [create a pull request from a fork](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork) to propose changes to an upstream repository.

1. Go to Compare Changes `https://github.com/YOUR-USERNAME/REPOSITORY-NAME/compare/` page
1. Select **compare across forks**
1. In the **base repository** drop-down menu, select `MASTER-USERNAME/REPOSITORY-NAME`
1. In the **head repository** drop-down menu, select your fork `YOUR-USERNAME/REPOSITORY-NAME`
1. Click **Create Pull Request**

If you are planning to do further work after the pull request, please use [Draft Pull Request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests#draft-pull-requests) feature.
