# Git

## Introduction

Git is local version control tool.

### Version control

(For good understaning i use the word layer, there is no official word layer in git).

You have a changes as layers one top of another. When you don't want the current change or you want any of the previous change, you can easily switch to it.

![Layers](https://www.professionalindemnity.co.uk/cms/photo/misc/three_flat__layers.png){:height="100px" width="100px"}

Each layer is created by you. How many layers you have is your own decision.

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

Add all modified files to staging area

```git
    git commit -m "<Reason-for-commit>"
```

Commit all files in staging area with the reason of what changes you did (In my words creating new layer)

## Communication between Git and Github

```git
    git push origin master
```

Push the commits of the master branch from local repository to Github

```git
    git pull origin master
```

Pull the commits of the master branch from Github to local repository
