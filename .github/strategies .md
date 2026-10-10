# strategies

---

## layout: default
title: When to Use What
parent: Undoing Git With...
nav_order: 5

# When to Use Different Strategies

### 📝 Summary

A breakdown of options to determine exactly which command fits your situation.

---

## 📊 Strategy Matrix

| Scenario / Goal | Recommended Tool | Command Example | Safe for Shared Remotes? |
| --- | --- | --- | --- |
| **Messed up a local file** and want it back to how it looked at the last commit. | `git checkout` | `git checkout -- player.cs` | ✅ Yes (Local only) |
| **A bug was discovered** in a commit pushed to GitHub last week. | `git revert` | `git revert a1b2c3d` | ✅ Yes (Safe for teams) |
| **Completely erase** your last 3 local unpushed commits and start over. | `git reset --hard` | `git reset --hard HEAD~3` | ❌ **No** (Local only) |
| **Project folder is cluttered** with random generated test builds and logs. | `git clean` | `git clean -fd` | ✅ Yes (Local only) |

---

## 🔗 External Resources & Further Reading

- [Atlassian Git Tutorial: Undoing Changes](https://atlassian.com/)
- [Pro Git Book: Git Basics - Undoing Things](https://git-scm.com/)