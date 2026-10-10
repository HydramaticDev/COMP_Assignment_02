---
layout: default
title: The Git Life Cycle
nav_order: 4
---

<!-- prettier-ignore-start -->

# The Git Life Cycle 
{: .no_toc }

Git keeps track of the metadata of files in the directory you created as you use Git inside your repository, acting as version control.
The Git Lifecycle is the stages that your files go through as you use Git with a repository. 


## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->

## Where Files Go

There are three locations files go through as you use Git Version Control.


1) The Working Directory

2) The Staging Area

3) The Repository

### 1: Working Directory

Once your repository is set up, Git becomes aware of the files in your Working Directory.

The Working Directory is the current state of the local folder you're working in. It changes as you add, delete, or modify files.

### 2: Staging Area

Git can add a current version of your Working Directory, or a specific file, to the Staging Area.

However, files in the working directory cannot be committed to the repository until they are staged.

### 3: The Repository

Once files are staged, they are ready to be committed to the Repository.

Committing saves the metadata of the staged files at that point in time and stores them in the .git folder. This essentially saves a snapshot of your repository.

You can include a commit message when committing to explain or describe the state of the repository at the time of the commit.


## Files

Files pass through four states during the Git Life Cycle:

1) Untracked

2) Unmodified

3) Modified

4) Staged

![The Git Life Cycle](lifecycle.png)

### Untracked

When a file is first created, it is untracked.

Git will not interact with any file unless explicitly told to, so untracked files are never committed or modified.

### Unmodified

Once a file is committed, its metadata is saved to Git. Since that version of the file is saved, it is now considered unmodified.

If you edit the file, it becomes modified.

### Modified

When a change is made to an unmodified file, it is considered modified. A modified file must be staged again before it can be committed.

### Staged

When a file is staged, it is tracked by Git and ready to be committed.

An untracked or modified file cannot be committed to a repository. Once it is added to the Staging Area, it is considered staged.
