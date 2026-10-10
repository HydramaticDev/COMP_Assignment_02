---
layout: default
title: The How And The Why Of Team GitHub Workflow
nav_order: 11
---

# The How and The Why of Team GitHub Workflow

A team Git workflow is an agreed-upon process that developers follow when making, sharing, reviewing, and integrating changes to a project. Using a consistent workflow helps teams collaborate efficiently, reduce mistakes, and maintain a reliable version of their project.

## Table of Contents

- [Centralized Workflow](./centralized-workflow)
- [Feature Branch Workflow](./feature-branch-workflow)
- [Forking Workflow](./forking-workflow)



## What Is a Team Git Workflow?

A team Git workflow describes how developers use Git to manage their work together. It establishes guidelines for creating branches, committing changes, sharing work through remote repositories, reviewing code, and merging changes into the main project.

For example, a game development team might have one developer working on player movement while another works on enemy behaviour. A clear workflow allows both developers to work independently before integrating their changes into the same project.

## Why Are Team Workflows Important?

Working on a project with multiple developers introduces challenges that are less common when working alone. Different team members may edit the same files, introduce incompatible changes, or accidentally overwrite work if collaboration is poorly organized.

A consistent Git workflow helps address these problems.

- **Organization:** Everyone understands where and how their changes should be made.
- **Collaboration:** Developers can work on different tasks without constantly interfering with one another.
- **Code review:** Changes can be checked by teammates before being integrated.
- **Conflict management:** Teams have a consistent process for identifying and resolving conflicting changes.
- **Accountability:** Commit histories and pull requests help track who made changes and why.

A workflow does not eliminate every mistake or merge conflict, but it gives the team a reliable process for handling them.

## Choosing a Git Workflow

Different projects benefit from different approaches. The best workflow depends on team size, project requirements, repository permissions, and how changes need to be reviewed.

### Centralized Workflow

The Centralized Workflow uses a shared repository where team members push and pull changes. Developers commonly work directly with a shared main branch or other shared branches.

This approach is relatively simple and can work well for small teams, but it requires coordination to avoid interfering with one another's work.

### Feature Branch Workflow

The Feature Branch Workflow gives each task or feature its own branch. Developers push their branches to a shared remote repository and create pull requests so teammates can review changes before they are merged into the main branch.

This approach keeps unfinished work separate from the main branch and is particularly useful when teams want structured code reviews.

### Forking Workflow

The Forking Workflow allows developers to create their own copies of a repository, called forks. They make changes in their forks and submit pull requests to propose those changes to the original repository.

This approach is especially useful for open-source projects and situations where contributors should not have direct write access to the original repository.

## Comparing the Workflows

| Workflow | How It Works | Common Use |
|---|---|---|
| Centralized | Developers collaborate through a shared repository. | Small teams with a simple collaboration process. |
| Feature Branch | Developers create task-specific branches and submit pull requests. | Teams that want isolated development and code review. |
| Forking | Developers work in separate repository copies and propose changes upstream. | Open-source projects and repositories with restricted write access. |

These approaches are not always mutually exclusive. For example, a team can use feature branches within its own repository while also maintaining a fork of an instructor's or organization's original repository.

## Best Practices for Team Collaboration

- Agree on a workflow before development begins.
- Use meaningful commit messages that explain the purpose of each change.
- Keep branches focused on specific tasks.
- Pull or fetch updates regularly to stay informed about changes.
- Review teammates' changes constructively.
- Resolve merge conflicts carefully instead of automatically choosing one side.
- Communicate when multiple developers need to modify the same files.

A good Git workflow helps a development team work toward the same goal while keeping changes organized, reviewable, and easier to maintain.