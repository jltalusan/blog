---
title: "Learning all about Git"
date:   2018-07-04 11:39:10 +0800
categories: "QAEngineers"
---

# Learning Git

## What is a Version Control?

Version control systems are a category of software tools that help a software team manage changes to source code over time. Version control software keeps track of every modification to the code in a special kind of database. If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members.

## What is Git?

Git is the most widely used modern version control system in the world today is Git. Git is a mature, actively maintained open source project originally developed in 2005 by Linus Torvalds, the famous creator of the Linux operating system kernel.

## Why Git?
It's free, widely used, secured and can be accessed wherever you are. 

## Feature Branch Workflow
One of the biggest advantages of Git is its branching capabilities. Unlike centralized version control systems, Git branches are cheap and easy to merge. This facilitates the feature branch workflow popular with many Git users. 

Feature branches provide an isolated environment for every change to your codebase. When a developer wants to start working on something—no matter how big or small—they create a new branch. This ensures that the master branch always contains production-quality code.

(sample guide)

## Distributed Development

In SVN (Apache Subversion - _software versioning/revision control system_), each developer gets a working copy that points back to a single central repository. Git, however, is a distributed version control system. Instead of a working copy, each developer gets their own local repository, complete with a full history of commits.

## Pull Requests

Many source code management tools such as Bitbucket enhance core Git functionality with pull requests. A pull request is a way to ask another developer to merge one of your branches into their repository. This not only makes it easier for project leads to keep track of changes, but also lets developers initiate discussions around their work before integrating it with the rest of the codebase.

## Git is Good, but how can I install it?

Download here : [Sourcetree](https://www.sourcetreeapp.com/) <br>
Create a BitBucket account : [BitBucket](https://bitbucket.org/product)

### Why these?
Sourcetree is made by Atlassian, the same company that made JIRA and owns Bitbucket

### Why do you need Sourcetree? 
Actually you don't need it since you can use git with your cmd, but it's better to use Git GUI apps like these for beginners to understand the flow better.

### Why do you need BitBucket? What does it do?
Well, BitBucket is a Git Repository. there's a lot of Git Repositories out there like GitHub and GitLab, but we're going to use BitBucket because that's what our company is using

### What is a Git Repository?
A Git repository is a virtual storage of your project. It allows you to save versions of your code, which you can access when needed. 

### Initializing a new repository: git init
To create a new repo, you'll use the git init command. git init is a one-time command you use during the initial setup of a new repo. Executing this command will create a new .git subdirectory in your current working directory. This will also create a new master branch. 

> cd /path/to/project

> git init

or 

> git init /path/to/project

### Cloning an existing repository: git clone
If a project has already been set up in a central repository, the clone command is the most common way for users to obtain a local development clone. Like git init, cloning is generally a one-time operation. Once a developer has obtained a working copy, all version control operations are managed through their local repository.

> git clone https://github.com/jltalusan/codeceptiondemo.git


### Saving changes to the repository: git add and git commit
Now that you have a repository cloned or initialized, you can commit file version changes to it. 

> cd /path/to/project

> git status

> git add /path/to/file/you/want/to/add/in/the/commit

or if you want to add all the changes to the commit type 'git add .'

> git commit -m 'insert some message here'

### Discarding changes that you don't want to be included in the commit: git checkout --

> cd /path/to/project

> git status

> git checkout - - /path/to/file/you/DONT/want/to/add/in/the/commit

> git add .

> git commit -m 'insert some message here'


### Adding changes to the repository itself
**WARNING**: Don't do this if you're not 100% sure that your code is working, never push to develop or master branch

> cd /path/to/project

> git checkout branchnameofyourproject

> git status

> git add /path/to/file/you/want/to/add/in/the/commit


or if you want to add all the changes to the commit type 'git add .'

> git commit -m 'insert some message here'

> git push - -set-upstream origin branchname
