# revert

---

## layout: default
title: Revert
parent: Undoing Git With...
nav_order: 3

# Undoing with Revert

### 📝 Summary

The safest option for shared remote team environments.

---

## 🪵 Safe Undoing via Revert

The `git revert` command creates a brand-new commit that does the exact opposite of a target commit.

- **Revert a specific commit safely:**
    
    ```bash
    git revert <commit-hash>
    ```
    
- This is the safest way to fix a mistake because it **does not rewrite history**. It leaves the original mistake in the log and explicitly documents the fix.