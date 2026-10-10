---
layout: default
title: Forking Workflow
parent: The How and The Why of Team GitHub Workflow
nav_order: 3
---

# Forking Workflow

The Forking Workflow is a Git collaboration approach in which developers create their own copies of a repository, called forks. They make changes in their own copies and submit pull requests to propose those changes to the original repository.

## What Is a Fork?

A fork is a separate copy of a repository hosted on a platform such as GitHub. It allows a developer to work on a project without needing direct write access to the original repository.

For example, if a developer wants to contribute a new feature to an open-source game, they can fork the game's repository, make their changes in their own copy, and propose those changes to the original project through a pull request.

A fork is different from a branch. A branch is a separate line of development within a repository, while a fork is a separate repository.

## Why Is the Forking Workflow Useful?

The Forking Workflow is especially useful when contributors should not be able to push directly to the original repository.

It provides several advantages:

- **Independent development:** Contributors can make changes without directly modifying the original repository.
- **Controlled access:** Contributors do not need write permission to the original repository to propose changes.
- **Code review:** Pull requests allow maintainers to review proposed changes.
- **Experimentation:** Developers can test ideas in their own forks without affecting the original project.
- **Open-source collaboration:** People outside a project team can contribute changes through a consistent review process.

## How Does It Work?

A typical Forking Workflow follows these steps:

1. Fork the original repository on GitHub.
2. Clone your fork to your computer.
3. Configure a remote for the original repository if you need to retrieve its updates.
4. Create a feature branch in your local clone.
5. Make changes and commit them.
6. Push the branch to your fork.
7. Open a pull request proposing changes to the original repository.
8. Address review feedback and wait for an authorized maintainer to merge the changes.

## Forking and Cloning a Repository

Forking is normally done through GitHub's website. After creating a fork, clone your fork to your local computer:

```bash
git clone https://github.com/your-username/game-project.git
```

This downloads your fork and creates a local repository.

When you clone a repository, Git normally configures a remote named `origin` pointing to the repository you cloned. In this example, `origin` points to your fork.

## Connecting to the Original Repository

To retrieve updates from the original repository, add it as a second remote, commonly named `upstream`:

```bash
git remote add upstream https://github.com/original-owner/game-project.git
```

Check your remote configuration:

```bash
git remote -v
```

You should see both `origin` and `upstream`, each pointing to its respective repository.

- `origin` points to your fork, where you can push your work.
- `upstream` points to the original repository, where you can retrieve updates.

The names `origin` and `upstream` are conventions. You can choose other names, but using these conventions makes the workflow easier to understand.

## Creating and Publishing a Feature Branch

Before starting a new task, update your local `main` branch with changes from the original repository if appropriate:

```bash
git switch main
git fetch upstream
git merge upstream/main
```

This fetches the original repository's updates and merges its `main` branch into your local `main` branch.

Next, create a branch for your task:

```bash
git switch -c feature/new-enemy
```

After making and committing your changes, push the branch to your fork:

```bash
git add .
git commit -m "Add new enemy behaviour"
git push -u origin feature/new-enemy
```

Your changes are now available on your fork on GitHub.

## Creating a Pull Request

After pushing your branch, create a pull request on GitHub.

Choose your fork and feature branch as the source, and select the original repository's appropriate target branch as the destination.

The original project's maintainers can review your changes, request modifications, and merge the pull request if they approve it.

A pull request does not automatically grant permission to change the original repository. It proposes changes for review by people who have the necessary permissions.

## Advantages of the Forking Workflow

- **Limited access requirements:** Contributors can participate without direct write access to the original repository.
- **Independent copies:** Work can be developed separately from the original project.
- **Structured review:** Maintainers can inspect proposed changes before accepting them.
- **Suitable for large communities:** Many contributors can work on the same project independently.
- **Reduced risk to the original repository:** Contributors cannot directly push to the original repository unless they also have appropriate permissions.

## Disadvantages of the Forking Workflow

- **Additional setup:** Contributors need to manage a fork and a local clone.
- **Synchronization:** Forks can fall behind the original repository and need to be updated.
- **More remote management:** Developers may need to understand both `origin` and `upstream`.
- **Review delays:** Pull requests may wait for maintainers to respond or approve them.

## Best Practices

- Keep your fork synchronized with the original repository.
- Use feature branches instead of making every change directly on your fork's `main` branch.
- Push changes to your own fork before opening a pull request.
- Keep pull requests focused on a specific task.
- Follow the original project's contribution guidelines.
- Resolve review feedback and merge conflicts before requesting final approval.

The Forking Workflow makes it possible for developers to contribute to projects independently while allowing maintainers to control which changes are accepted into the original repository.