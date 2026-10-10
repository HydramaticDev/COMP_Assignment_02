---
layout: default
title: Git Fundamentals
nav_order: 5
---

# Git Fundamentals
{: .no_toc }

By the end of this page, you will be able to:

1) Set up Git to associate your work with your name and email address.

2) Create new repositories and add files to them.

3) View the history of your project and compare it to its current state.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

# Configuring Git

After installing Git, configure the name and email address that will be associated with your commits:

`git config --global user.name "Your Name"`
`git config --global user.email "your.email.example.com"`

These are the commands you use to configure it.

# Initializing a Repository

To create a new Git repository in the current working directory, use the initialization command:

`git init`

Git defaults to using the word "master" (as in "master copy" or "master recording") for the main branch, but you can rename it:

`git branch -m main`

{: .note } Creating a Git repository adds an invisible .git folder. To see it, enable "show hidden items" in your file explorer.

## Checking Your Repository's Status

The status command displays the current state of the repository. This is helpful for checking whether you are up to date with changes on a remote repository, or whether you have modified files to stage or commit:

`git status`

# Staging and Committing Files

As you make changes to your code, you commit those changes to your Git repository. 
Before you can commit, you must add new or changed files to the staging area.

For example, to stage a file named information.txt:

`git add information.txt`

To stage all changed files:

`git add .`

The add command also accepts sub-folders:

`git add docs/information.txt`

To add all files of a certain type, use a wildcard character:

`git add docs/*.txt`

This adds all text files in the docs folder.

## Committing Staged Files

Commit your staged changes with a commit message:

`git commit -m "Your details of the changes you added."`

For more complex changes, include a short title followed by a longer description:
`git commit -m "Title" -m "More Verbose description here."`

# Log and Diff

Review all previous commits with:

`git log`

Each entry in the log shows:

1) The commit hash.

2) Who made the commit.

3) When it was made.

4) The commit message.

Compare the differences between the current files and the last commit with:

`git diff`

You can also compare specific files:

`git diff information.txt`

Or specific folders:

`git diff ./docs`

# Using a .gitignore File

Often when working on a project, there are files you don't want saved in your repository. Examples include:

1) Files that contain secrets like API keys.

2) Temporary files.

3) Build files and folders.

4) Hidden OS files like Thumbs.db (Windows).

For these situations, use a .gitignore file. These files contain a list of rules that determine which files to skip when staging and committing. An example .gitignore might look like this:

```
# Ignore specific files. (Note that comments start with: #)
Thumbs.db
# Wildcards: Ignore all .exe files.
*.exe
# Exception to wildcards: Do track the special.exe file.
!special.exe
# Ignore all files in any folder called build.
build/
# Ignore all .pdf files in the doc/ folder and any of its sub-folders.
doc/**/*.pdf
```