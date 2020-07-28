# Git

## Introduction

Git is local version control tool.

### Cheatsheet

[Click here](#Cheatsheet-for-commands)

### Version control

(For good understaning i use the word layer, there is no official word layer in git).

<img src="https://www.professionalindemnity.co.uk/cms/photo/misc/three_flat__layers.png" alt="Layers" title="Layers" width="200px" style="float:right;padding-left:20px"/>

You have a changes as layers one top of another. New layer go top of every layer. When you don't want the current change or you want any of the previous change, you can easily switch to it.

Each layer is created by you. Whenever you feel it is time to create a layer go and do it. Recommend to do frequent commits instead of doing bulk changes in one commit.

### Stages of working with git

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcS9XU-mhS1xiQ9Us3SOAmkg7Ggdwj_Ln_8yqg&usqp=CAU" alt="Layers" title="Layers" width="100px" style="float:right;padding-left:20px"/>

There are three stages in git,

1. Files you are working on
2. Staging area (Contain files for creating next layer)
3. Save the current stage(creating one layer)

## Initializing local repository

```git
    git init
```

Once a project to initialize a local repository.

## Connect local repository with Github repository

```git
    git remote add origin <github-repo-url>
```

Connect a local repository with github repository once a project.

```git
    git clone <github-repo-url>
```

Setup existing github repository for working in your local system (Simply download the repository from github).

```git
    git remote set-url origin <github-repo-url>
```

Changing a github repository url.

## Basic git commands

```git
    git status
```

See the status of the local repository.

```git
    git add <file-name>
```

Add a specific file to staging area.

```git
    git add .
```

Add all modified and newly created files to staging area.

```git
    git commit -m "<Reason-for-commit>"
```

Commit all files in staging area with the reason of what changes you did (In my words creating new layer).

```git
    git commit - a -m "<Reason-for-commit>"
```

Add all modified files to stage and commit them.

**Note: Newly created files are not be taken when you use this command for commit**

## Communication between Git and Github

```git
    git push origin master
```

Push the commits of the master branch from local repository to Github.

```git
    git pull origin master
```

Pull the commits of the master branch from Github to local repository.

## Branch

```git
    git branch
```

Shows all branch in your repository. Master is the default branch.

```git
    git branch <branch-name>
```

Create a new branch. When you create a branch by default it consits all files in master branch.

```git
    git checkout <branch-name>
```

Switching between branchs.

```git
    git merge <branch-name>
```

Merge all changes from the branch you specified to current branch you are working.

```git
    git branch -d <branch-name>
```

Delete a branch.

## Logs

```git
    git log --oneline
```

Shows each commit with id and reason(short details).

**Note: Enter to continue; q to exit**

```git
    git log
```

Shows details about each commit.

**Note: Enter to continue; q to exit**

## Undo

```git
    git restore --staged <file-name>
```

Unstage or remove the file from the stage area.

```git
    git restore --staged .
```

Unstage or remove all the file from the stage area.

```git
    git reset <commit-id>
```

Switch to commit(layer) you specified. The commit after the sepcific commit-id will be deleted.

**You will find commit-id in logs**

```git
    git revert <commit-id>
```

Create new commit which contains the changes in that commit you specified. Safe way of doing because you can switch if you don't want it. Incase of reset it won't.

**You will find commit-id in logs**

```git
    git checkout <commit-id>
```

Simply view the changes in specific commit. you cant switch back to old stage using **git checkout \<branch-name\>**

**You will find commit-id in logs**

## difference

```git
    git diff
```

Show changes between last staged files and working files.

```git
    git diff --staged
```

Show changes between last commit and staged files.

## Cheatsheet for commands

```git
git init

git status
git add <file-name>
git add .
git commit -m "<Reason-for-commit>"
git commit -a -m "<Reason-for-commit>"

git remote add origin <github-repo-url>
git remote set-url origin <github-repo-url>
git clone <github-repo-url>

git pull origin master
git push origin master

git branch
git branch <branch-name>
git checkout <branch-name>
git merge <branch-name>
git branch -d <branch-name>

git log
git log --oneline

git restore --staged <file-name>
git restore --staged .
git reset <commit-id>
git revert <commit-id>
git checkout <commit-id>

git diff
git diff --staged
```
