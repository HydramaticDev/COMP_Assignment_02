---
layout: default
title: Feature Branch Workflow
parent: The How And The Why Of Team GitHub Workflow
nav_order: 2
---

# Feature Branch Workflow

The Feature Branch Workflow is a Git collaboration approach in which each new feature, fix, or task is developed on its own branch. Developers push their branches to a shared remote repository and use pull requests to review changes before merging them into the main branch.

## What Is the Feature Branch Workflow?

In the Feature Branch Workflow, the `main` branch is kept separate from unfinished development work. Instead of making changes directly on `main`, developers create branches for individual tasks.

For example, a game development team might create separate branches for player movement, enemy AI, and menu design. Each developer can work on their assigned task without immediately changing the main version of the project.

Once the work is ready, the developer pushes the branch to GitHub and opens a pull request so teammates can review it.

## How Does It Work?

A typical Feature Branch Workflow follows these steps:

1. Update your local `main` branch.
2. Create a new branch for your task.
3. Make changes and commit them on that branch.
4. Push the branch to GitHub.
5. Create a pull request targeting `main`.
6. Have teammates review the changes and request adjustments if necessary.
7. Merge the pull request after approval.
8. Update your local repository before beginning your next task.

### Creating a Feature Branch

First, switch to `main` and retrieve the latest changes:

```bash
git switch main
git pull origin main
```

Create a new branch for your task:

```bash
git switch -c feature/player-movement
```

The `git switch -c` command creates a new branch and switches to it immediately.

### Committing and Pushing Changes

After modifying your files, stage and commit your changes:

```bash
git add .
git commit -m "Add player movement"
```

Push the feature branch to GitHub:

```bash
git push -u origin feature/player-movement
```

The `-u` option establishes an upstream tracking relationship for the branch, making future pushes easier.

### Creating a Pull Request

Once your branch has been pushed, open GitHub and create a pull request targeting the repository's `main` branch.

A pull request allows teammates to inspect your changes, discuss potential improvements, and request modifications before the work is merged.

After approval, an authorized teammate merges the pull request into `main`.

**Important:** A pull request is a GitHub collaboration feature, not a Git CLI command. Git handles branches and commits, while GitHub provides the interface for reviewing and merging proposed changes.

## Advantages of the Feature Branch Workflow

- **Isolation:** Each task is developed separately from the main branch.
- **Code review:** Teammates can examine changes before they are integrated.
- **Safer main branch:** Unfinished work stays out of the main branch until it is ready.
- **Parallel development:** Multiple developers can work on different tasks at the same time.
- **Clear history:** Branches, commits, and pull requests help explain how changes were developed.

This workflow is particularly useful for teams that want a consistent review process and a more organized development cycle.

## Disadvantages of the Feature Branch Workflow

- **More coordination:** Developers must keep track of branches, pull requests, and reviews.
- **Merge conflicts:** Changes made on different branches can still conflict when integrated.
- **Stale branches:** A feature branch may fall behind `main` if it remains active for too long.
- **Review delays:** Work may wait for approval before it can be merged.

Keeping branches focused and communicating with teammates can help reduce these challenges.

## Keeping a Feature Branch Up to Date

While working on a feature, other developers may merge changes into `main`. You may need to integrate those updates into your branch before merging your own work.

One common approach is to fetch the latest remote changes and merge `main` into your feature branch:

```bash
git fetch origin
git switch feature/player-movement
git merge origin/main
```

If conflicts occur, resolve them before continuing.

Another approach is rebasing, but teams should agree on which integration strategy to use. Avoid rebasing shared branches that other developers are already relying on unless your team understands the implications.

## Best Practices

- Create a separate branch for each feature, fix, or documentation task.
- Start new branches from an up-to-date `main` branch.
- Use meaningful branch names and commit messages.
- Push your branch regularly.
- Keep pull requests focused and reasonably small.
- Review teammates' changes constructively.
- Do not merge your own pull request when your team requires another member to approve and merge it.
- Delete completed feature branches when they are no longer needed, following your team's conventions.

The Feature Branch Workflow helps teams develop changes independently while maintaining a controlled process for reviewing and integrating work into the main project.