---
layout: default
title: Centralized Workflow
parent: The How And The Why Of Team GitHub Workflow
nav_order: 1
---

# Centralized Workflow

The Centralized Workflow is a Git collaboration approach in which developers share a central repository. Team members push their commits to the shared repository and pull updates made by others, allowing everyone to contribute to the same project.

## What Is the Centralized Workflow?

In the Centralized Workflow, the team works from a common remote repository, usually hosted on GitHub. Each developer has a local clone of that repository and uses it to make commits before sharing their changes.

Unlike the Feature Branch Workflow, the simplest version of the Centralized Workflow allows developers to commit and push directly to a shared main branch.

For example, a small game development team might use a shared repository for a simple prototype where each member contributes code, levels, or documentation.

## How Does It Work?

A typical Centralized Workflow follows these steps:

1. Clone the shared repository to your computer.
2. Make changes to your project files.
3. Stage and commit your changes locally.
4. Pull or fetch updates from the remote repository to check for changes made by teammates.
5. Push your commits to the shared repository.
6. Repeat the process as development continues.

To clone a repository, use:

```bash
git clone https://github.com/username/game-project.git
```

After making changes, stage and commit them:

```bash
git add .
git commit -m "Update player movement"
```

Before pushing, retrieve and integrate any relevant remote changes:

```bash
git pull origin main
```

Then push your commits:

```bash
git push origin main
```

These commands assume that you are working on `main` and have permission to push to it. A team may instead use shared integration branches or additional protections.

## Advantages of the Centralized Workflow

- **Simplicity:** The team follows a straightforward process using a shared repository.
- **Easy access:** Team members can retrieve the latest committed work from one central location.
- **Shared history:** Commits are collected in a common project history.
- **Less branch management:** A basic centralized setup may require fewer branches and less coordination around pull requests.

This can make the workflow suitable for small projects where changes are relatively easy to coordinate.

## Disadvantages of the Centralized Workflow

- **Potential conflicts:** Multiple developers may modify the same files or lines.
- **Coordination requirements:** Team members need to communicate when working on overlapping tasks.
- **Risk to the main branch:** Pushing unfinished or incorrect changes directly to `main` can affect everyone.
- **Less structured review:** A simple setup does not automatically require another developer to review changes.

Branches, repository permissions, and pull requests can help reduce these risks, even when a team uses a centralized repository.

## When Should You Use It?

The Centralized Workflow can work well for small teams, simple projects, or situations where developers can coordinate their changes easily.

For example, a team creating a small game prototype might use one shared repository and coordinate who is editing each script.

For larger projects or teams that require formal reviews, a Feature Branch Workflow often provides better separation between unfinished work and the main branch.

## Best Practices

- Communicate with teammates before making overlapping changes.
- Commit regularly with clear, descriptive messages.
- Retrieve relevant remote updates before pushing.
- Resolve conflicts carefully when they occur.
- Protect the main branch when project stability is important.
- Consider branches and pull requests if direct collaboration becomes difficult to manage.

The Centralized Workflow offers a simple way for developers to share work through a common repository, but it works best when team members communicate and coordinate their changes effectively.