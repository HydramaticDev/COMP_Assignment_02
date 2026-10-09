# Stashing

---

## layout: default
title: Stashing
nav_order: 11

# Stashing: Temporarily Shelving Work

### 📝 Summary

Learn how to use `git stash` to safely clear your working directory and switch branches without losing your half-finished progress.

---

## 🔍 Table of Contents

{:toc}

---

## 💾 How to Use Stashing in Git Bash

When you are in the middle of a task (like adjusting a gameplay script or tweaking a material) and need to pull changes or switch branches immediately, `git stash` saves your dirty working directory state without making a permanent commit.

- **Save current changes to a stash:**
    
    ```bash
    git stash save "Describe your temporary work here"
    ```
    
- **View your saved stashes:**
    
    ```bash
    git stash list
    ```
    
- **Apply the most recent stash and remove it from the list:**
    
    ```bash
    git stash pop
    ```
    
- **Apply a specific stash from the list:**
    - ⚠️ *Git Bash Warning:* You **must** wrap the stash index argument in single quotes (`'stash@{1}'`). Leaving quotes out will cause Git Bash to throw a shell expansion error.
    
    ```bash
    git stash apply 'stash@{1}'
    ```
    
- **Discard all stashed changes:**
    
    ```bash
    git stash clear
    ```
    

---

## 🔗 External Resources

- [Git Documentation: git-stash](https://git-scm.com/)