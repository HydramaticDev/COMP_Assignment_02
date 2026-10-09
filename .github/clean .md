# clean

---

## layout: default
title: Clean
parent: Undoing Git With...
nav_order: 4

# Undoing with Clean

### 📝 Summary

Brooming away build files, logs, and untracked clutter.

---

## 🪵 Sweeping the Directory via Clean

The `git clean` command removes untracked files (files that have never been added to Git). It does not affect tracked files.

- **Dry Run (See what will be deleted):**
    
    ```bash
    git clean -n
    ```
    
- **Force Delete untracked files:**
    
    ```bash
    git clean -f
    ```
    
- **Force Delete untracked files and folders:**
    
    ```bash
    git clean -fd
    ```