---
layout: default
title: Remote Repositories
nav_order: 10
---

# Remote Repositories

A remote repository is a version of your Git repository hosted somewhere other than your local computer, such as GitHub. Remote repositories allow developers to share code, collaborate with teammates, and keep their work synchronized across multiple computers.

## Table of Contents

- [Adding / Configuring A GitHub Remote](./adding-configuring-a-github-remote)
- [Pushing and Pulling](./pushing-and-pulling)



## What Is a Remote Repository?

A local repository stores your project's version history on your own computer. A remote repository stores a separate copy of that history on another computer or server that you can connect to over a network.

For example, if you are working on a game with a team, your local repository contains your own work, while a remote repository on GitHub allows your teammates to access shared changes.

A remote repository does not automatically update whenever you make changes locally. You must use Git commands such as `git push` and `git pull` to synchronize changes.

## Why Are Remote Repositories Important?

Remote repositories are useful for several reasons:

- **Collaboration:** Team members can share commits and contribute to the same project.
- **Backup:** A remote copy provides another place where your committed work is stored.
- **Synchronization:** Developers can share updates between different computers.
- **Project management:** Platforms such as GitHub provide tools for reviewing changes, managing branches, and creating pull requests.

For example, a game developer can push changes to a remote repository at school and pull those changes onto their home computer to continue working.

## Local vs. Remote Repositories

Although local and remote repositories contain Git history, they serve different purposes.

| Local Repository | Remote Repository |
|---|---|
| Stored on your computer. | Hosted elsewhere, such as on GitHub. |
| Used to develop and commit changes locally. | Used to share committed changes with others. |
| Can be used without an internet connection. | Usually accessed over a network. |
| Changes are not automatically shared with teammates. | Provides a shared location for exchanging changes. |

Remember that a remote repository is not necessarily the original or main repository. It is simply another repository that your local repository knows how to access.

## Understanding Remote Names

Git allows you to assign a short name to a remote repository so you do not need to repeatedly type its full URL.

Two common remote names are:

- `origin`: Usually the default name for the remote repository you cloned from.
- `upstream`: Often used to refer to the original repository from which a fork was created.

These names are conventions rather than special Git keywords. You can use other names if you choose.

For example, if you fork a GitHub repository for a team project, your team's fork might be called `origin`, while the instructor's original repository might be called `upstream`.

## Viewing Remote Repositories

You can use Git commands to check which remote repositories are connected to your local repository.

To list the names of your configured remotes, use:

```bash
git remote
```

To display the remote names along with their URLs, use:

```bash
git remote -v
```

The `-v` option means verbose. It displays the URLs Git uses to fetch changes from and push changes to each remote.

Example output:

```text
origin    https://github.com/username/game-project.git (fetch)
origin    https://github.com/username/game-project.git (push)
```

This output shows that the remote named `origin` is connected to the specified GitHub repository.

## How Remote Repositories Work

Remote repositories work alongside your local repository to help you exchange changes with other developers.

A typical workflow looks like this:

1. Make changes to files in your local project.
2. Stage and commit your changes to record them in your local Git history.
3. Push your commits to a remote branch so other team members can access them.
4. Fetch or pull remote changes to retrieve updates made by other developers.
5. Integrate those updates into your local work as needed.

For example, if one team member finishes a new player movement system and pushes their commits to GitHub, another team member can retrieve those changes and continue working with the updated project.

## Best Practices

- Push important commits regularly so your team can access your work.
- Fetch or pull updates regularly to keep your local branches up to date.
- Use `git remote -v` to verify that your repository is connected to the correct remote.
- Understand the difference between `origin` and `upstream` when working with forks.
- Remember that committing changes locally does not automatically upload them to GitHub.

Remote repositories are a fundamental part of collaborative Git development. Understanding how they work makes it easier to share code, coordinate with teammates, and manage projects using GitHub.