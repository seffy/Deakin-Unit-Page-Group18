# 🛠️ Git Restore Steps 

## 1. 🔍 Check the History
View recent commits:
```bash
git log --oneline
```

Or view all history, even resets:
```bash
git reflog
```
✅ Find a commit where the project was correct.

---

## 2. 🎯 Find the Safe Commit
Pick the commit hash (e.g., `dabd37c`) you want to restore to.

---

## 3. 🔄 Restore Options

### Option A: Restore One File
```bash
git checkout commit-hash -- filename
```
Example:
```bash
git checkout dabd37c -- index.html
```
✅ Restores only the selected file.

---

### Option B: Restore Full Project
```bash
git reset --hard commit-hash
```
Example:
```bash
git reset --hard dabd37c
```
✅ Fully resets your local project to that commit.

---

## 4. 📤 Push the Corrected Version
After fixing:
```bash
git push origin main --force
```
✅ Force push updates GitHub with your corrected local version.

---

# 📋 Quick Restore Summary

| Situation | Command |
|:----------|:--------|
| Check history | `git log` or `git reflog` |
| Restore one file | `git checkout commit-hash -- filename` |
| Restore full project | `git reset --hard commit-hash` |
| Push fixed project | `git push origin main --force` |

---

# 🚨 Important Reminders
- Always use `git log` or `git reflog` to check first.
- Communicate with the team before using `--force`.
- Backup your folder manually if unsure.

