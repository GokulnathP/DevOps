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

There are three stages in git

1. Files you are working on
2. Staging area (Contain files for creating next layer)
3. Save the current stage(creating one layer)

## Initializing local repository

```git
    git init
```

Once a project to initialize a local repository

## Connect local repository with Github repository

```git
    git remote add origin <github-repo-url>
```

Connect a local repository with github repository once a project

```git
    git clone <github-repo-url>
```

Setup existing github repository for working in your local system (Simply download the repository from github).

```git
    git remote set-url origin <github-repo-url>
```

Changing a github repository url

## Basic git commands

```git
    git status
```

See the status of the local repository

```git
    git add <file-name>
```

Add a specific file to staging area

```git
    git add .
```

Add all modified and newly created files to staging area

```git
    git commit -m "<Reason-for-commit>"
```

Commit all files in staging area with the reason of what changes you did (In my words creating new layer)

```git
    git commit - a -m "<Reason-for-commit>"
```

Add all modified files to stage and commit them.

**_ Note: Newly created files are not be taken when you use this command for commit_**

## Communication between Git and Github

```git
    git push origin master
```

Push the commits of the master branch from local repository to Github

```git
    git pull origin master
```

Pull the commits of the master branch from Github to local repository

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
```
