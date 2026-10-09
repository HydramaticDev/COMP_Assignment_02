# Checkout

---

## layout: default
title: Checkout
parent: Undoing Git With...
nav_order: 1

# Undoing with Checkout

### 📝 Summary

How to use `git checkout` to discard local changes or review historical file versions.

---

## 🪵 Discarding Changes with Checkout

The `git checkout` command changes the files in your working directory to match a previous state or commit.

- **Discard uncommitted changes in a specific file:**
    
    ```bash
    git checkout -- <filename>
    ```
    
- **View a specific file from a previous commit:**
    
    ```bash
    git checkout <commit-hash> -- <filename>
    ```
    
- ⚠️ **Warning:** Discarding local changes with checkout is **permanent**. Your unsaved work cannot be recovered.