---
layout: default
title: Adding / Configuring a GitHub Remote
parent: Remote Repositories
nav_order: 1
---

# Adding / Configuring a GitHub Remote

A Git remote connects your local repository to another repository hosted elsewhere, such as GitHub. Configuring a remote allows you to push your commits to GitHub and retrieve changes made by other developers.

## What Is a GitHub Remote?

A GitHub remote is a named connection between your local Git repository and a repository hosted on GitHub.

When you create or clone a project, Git can use a remote to keep track of where changes should be sent and retrieved from.

For example, if you are developing a game with a team, you can connect your local project to your team's GitHub repository. This allows you to share your committed work and access changes made by your teammates.

A remote does not automatically synchronize your files. You must use commands such as `git push`, `git pull`, and `git fetch` to exchange changes.

## Adding a Remote Repository

To connect a local Git repository to a GitHub repository, you first need the repository's URL. You can find this by opening the repository on GitHub and selecting the **Code** button.

Once you have the URL, use the following command:

```bash
git remote add origin https://github.com/username/game-project.git
```

In this command:

- `git remote add` creates a new remote connection.
- `origin` is the name assigned to the remote.
- The URL identifies the GitHub repository you want to connect to.

Replace the example URL with your own repository's URL.

The name `origin` is a common convention, but you can choose another name if needed.

**Important:** Run this command from inside your local Git repository. If you cloned the repository from GitHub, a remote named `origin` is usually already configured, so you generally do not need to add it again.

## Viewing Configured Remotes

After adding a remote, you can check whether it was configured correctly.

To list the names of your remotes, use:

```bash
git remote
```

To display the names and URLs of your remotes, use:

```bash
git remote -v
```

The `-v` option means verbose. It displays the URLs Git uses for fetching and pushing.

Example output:

```text
origin  https://github.com/username/game-project.git (fetch)
origin  https://github.com/username/game-project.git (push)
```

This confirms that your local repository has a remote named `origin` connected to the specified GitHub repository.

## Changing a Remote URL

If a repository has moved or you need to connect your local project to a different GitHub repository, you can change the URL of an existing remote.

Use:

```bash
git remote set-url origin https://github.com/username/new-game-project.git
```

This changes the URL associated with `origin` without creating a new remote.

You can then verify the change with:

```bash
git remote -v
```

**Remember:** Changing a remote URL changes where Git sends and retrieves changes. Make sure the new URL points to the repository you actually intend to use.

## Using Multiple Remotes

A local Git repository can have more than one remote connection. This is particularly useful when working with forks.

For example, when your team forks an instructor's original repository, you might use:

- `origin` for your team's fork.
- `upstream` for the instructor's original repository.

You can add the original repository as another remote using:

```bash
git remote add upstream https://github.com/instructor/original-project.git
```

You can then view both remotes with:

```bash
git remote -v
```

This setup allows you to push your team's work to its own repository while fetching updates from the original repository when necessary.

The names `origin` and `upstream` are conventions rather than special Git keywords. Their meaning depends on how you configure them.

## Removing a Remote

If you no longer need a remote connection, you can remove it with:

```bash
git remote remove origin
```

This removes the remote named `origin` from your local repository's configuration.

It does **not** delete the repository hosted on GitHub or erase your local commits. However, Git will no longer use that remote name to push or fetch changes.

Use this command carefully, especially if `origin` is your team's main GitHub repository.

## Best Practices

- Use `git remote -v` to check which repositories your local project is connected to.
- Use the correct GitHub URL when adding or changing a remote.
- Remember that cloned repositories usually already have an `origin` remote.
- Use separate remotes when working with forks that need to track an original repository.
- Double-check your remote configuration before pushing commits to avoid sending changes to the wrong repository.

Configuring Git remotes correctly is an important part of working with GitHub. Once your remotes are set up, you can push your work, retrieve updates, and collaborate with other developers more effectively.