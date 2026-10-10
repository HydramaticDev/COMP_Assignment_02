---
layout: default
title: Pushing And Pulling
parent: Remote Repositories
nav_order: 2
---

# Pushing and Pulling

Pushing and pulling allow developers to synchronize their local Git repositories with remote repositories hosted on services such as GitHub. These commands are essential for sharing work, retrieving updates, and collaborating with teammates.

## Pushing Changes

The `git push` command uploads local commits to a remote repository. This allows other team members to access your changes once they have been pushed to a branch they can access.

For example, to push your local `main` branch to the remote repository named `origin`, use:

```bash
git push origin main
```

In this command:

- `git push` uploads your local commits.
- `origin` identifies the remote repository.
- `main` identifies the branch being pushed.

When working with a new feature branch, you can publish it and configure its upstream tracking branch using:

```bash
git push -u origin feature/player-movement
```

The `-u` option establishes a tracking relationship between your local branch and its remote counterpart, making future pushes and pulls simpler.

**Important:** Git can reject a push if the remote branch contains changes that your local branch does not have. You may need to retrieve and integrate those changes before pushing again.

## Pulling Changes

The `git pull` command retrieves changes from a remote repository and integrates them into your current local branch.

For example, to pull updates from the remote `main` branch, use:

```bash
git pull origin main
```

This command fetches updates from `origin` and integrates the remote `main` branch into your current branch. Depending on your Git configuration and branch history, Git may fast-forward or merge the changes, or it may require you to resolve conflicts.

Pulling is especially useful when working with a team because other developers may have pushed changes since your last update.

**Important:** Make sure you understand which branch you are currently on before pulling. The command integrates changes into your current branch, which may not be `main`.

## Fetching vs. Pulling

Although fetching and pulling are related, they do different things.

The `git fetch` command downloads updates from a remote repository without integrating those changes into your current branch.

```bash
git fetch origin
```

After fetching, you can inspect the incoming changes before deciding how to integrate them.

By contrast, `git pull` fetches remote changes and then integrates them into your current branch.

In simple terms:

- **Fetch:** Retrieve updates so you can inspect them.
- **Pull:** Retrieve updates and integrate them into your current branch.

Fetching is useful when you want to review your teammates' changes before incorporating them into your own work.

## Working with Feature Branches

In a team using the feature branch workflow, developers generally push their work to separate feature branches instead of directly pushing to `main`.

For example, suppose you are adding a new player movement system to a game. You might create a branch called `feature/player-movement`, make your changes, and commit them locally.

To push that branch to GitHub, use:

```bash
git push -u origin feature/player-movement
```

Once the branch is pushed, you can create a pull request on GitHub asking your teammates to review your changes before they are merged into `main`.

Before starting additional work, you should also retrieve the latest changes from the main branch when appropriate:

```bash
git switch main
git pull origin main
```

You can then create a new feature branch from the updated `main` branch.

This workflow helps keep individual tasks separate and reduces the risk of unreviewed changes being added directly to the main branch.

## Common Problems

### Push Rejected

A push may be rejected when the remote branch contains commits that your local branch does not have.

You may need to fetch and integrate the remote changes before trying again. Avoid forcing a push unless you understand the consequences, because it can overwrite remote history.

### Merge Conflicts

A pull can result in a merge conflict if Git cannot automatically reconcile changes made to the same parts of a file.

When this happens, open the conflicting files, decide which changes should be kept, resolve the conflict markers, and commit the resolution if Git requires a merge commit.

### Authentication Problems

GitHub may reject a push if you are not properly authenticated or do not have permission to write to the repository.

Check that you are signed in using your configured Git authentication method and that you have the necessary repository access.

## Best Practices

- Commit your changes before pushing them to GitHub.
- Push feature branches regularly so your team can access your work.
- Pull or fetch updates regularly to stay informed about changes made by teammates.
- Check your current branch before running push or pull commands.
- Use pull requests to review changes before merging them into `main`.
- Avoid force-pushing shared branches unless your team has agreed that it is appropriate.

Pushing and pulling are fundamental parts of collaborative Git development. Understanding when to use each command helps developers share work safely, keep their repositories synchronized, and work effectively as a team.