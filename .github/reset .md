# reset

---

## layout: default
title: Reset
parent: Undoing Git With...
nav_order: 2

# Undoing with Reset

### 📝 Summary

Using `git reset` to shift your branch pointer backward through history.

---

## 🪵 Branch Manipulation via Reset

The `git reset` command moves your current branch pointer back to a specific commit.

- **Soft Reset (Keeps changes staged):**
    
    ```bash
    git reset --soft <commit-hash>
    ```
    
- **Mixed Reset (Default - Keeps changes unstaged):**
    
    ```bash
    git reset <commit-hash>
    ```
    
- **Hard Reset (Destroys all changes):**
    - ⚠️ *Git Bash Warning:* Use the tilde modifier `HEAD~3`. Avoid using the caret symbol (`HEAD^`) because it acts as an escape character in Windows environments and causes terminal bugs.
    
    ```bash
    git reset --hard HEAD~3
    ```
    
- ⚠️ **Warning:** Never use `git reset --hard` on commits that have already been pushed to GitHub.