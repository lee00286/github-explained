# Sync and Reset the Fork

## Table of Contents
- [How to Sync](#how-to-sync)
- [How to Reset](#how-to-reset)

## How to Sync

### Sync a Fork

[Syncing a Fork](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/syncing-a-fork) keeps your repository be up-to-date with the upstream repository.

Open Terminal and change the current working directory to your local project.

Type `git fetch upstream` to fetch the branches and their changes (commits) from the upstream repository. If there's no change, then nothing will be printed. If there's any change, the progress will be shown like the lines below.

```
$ git fetch upstream
> remote: Counting objects: 75, done.
> remote: Compressing objects: 100% (53/53), done.
> remote: Total 62 (delta 27), reused 44 (delta 9)
> Unpacking objects: 100% (62/62), done.
> From https://github.com/OWNER-USERNAME/REPOSITORY-NAME
>  * [new branch]      master     -> upstream/master
```

Type `git checkout master` to check out your fork's local master branch. If you are already on master, `Already on 'master'` will be printed.

```
$ git checkout master
> Switched to branch 'master'
```

Type `git merge upstream/master` to merge the changes from upstream/master into your local master branch. Your local changes will not be lost while your fork's master branch syncs with the upstream repository. Below lines are the examples of the progress.

```
$ git merge upstream/master
> Updating a422352..5fdff0f
> Fast-forward
>  README                    |    3 ---
>  README.md                 |    5 +++++
>  2 files changed, 5 insertions(+), 3 deletions(-)
>  delete mode 100644 README
>  create mode 100644 README.md
```

## How to Reset

### Reset a Fork

:exclamation: If you have any local changes that haven't been pushed will be lost, they will be lost.

:exclamation: Terminal will hold the task immediately without your re-confirmation.

Open Terminal and change the current working directory to your local project.

Type `git fetch upstream` and `git checkout master`. 

Type `git reset --hard upstream/master` and `git push origin master --force`. Then, your forked master branch and local clone will be overwritted by the upstream.

```
$ git remote add upstream /url/to/original/repo
$ git fetch upstream
$ git checkout master
$ git reset --hard upstream/master  
$ git push origin master --force 
> Total 0 (delta 0), reused 0 (delta 0)
> To https://github.com/YOUR-USERNAME/REPOSITORY-NAME.git
 + b4e299a...fc190ae master -> master (forced update)
```
