# Workflow for Updating Project


*IMPORTANT *
- Pull main branch frequently before starting work.
- Work on your own feature branch — avoid direct edits to main.
- Commit often after meaningful changes (not after every minor edit).
- Communicate issues early (don’t wait until something breaks).

---



### 1. 📍 Check Which Branch You're On
Before starting, make sure you’re on main

```bash
git branch
```
✅ Shows your current branch.

---

### 2. 🔄 Make Sure Your `main` Is Updated
```bash
git checkout main
git pull origin main
```
✅ Ensure you have the latest updates from GitHub.

---

### 3. 🌱 Create a New Branch for Your Updates
```bash
git checkout -b add-footer
```
✅ Create and switch to your feature branch.

---

### 4. 🛠️ Make Your Changes
- Edit HTML, CSS, JS files as needed.
- Save your changes locally.

---

### 5. 📥 Stage and Commit Your Changes
```bash
git add .
git commit -m "Update footer layout and styles"
```
✅ Save changes to your local repository.

---

### 6. 🚀 Push Your Branch to GitHub
```bash
git push -u origin add-footer
```
✅ Push and link the branch to GitHub.

---
* Notify the Team Leader to merge it after checking. *
- Only Team Leader will merge branches into main.
- Team Leader will handle merge conflicts if needed.
---

### 7. 🔄 Update Your Main Branch Again
```bash
git checkout main
git pull origin main
```
✅ Make sure your main is the latest before merging.

---

### 8. 🔀 Merge Your New Branch into Main
```bash
git merge add-footer
```
✅ Combine your updates into main.

---

### 9. 📤 Push the Updated Main Back to GitHub

```bash
git push 
```

OR 

```bash
git push origin main
```
✅ Final push to update GitHub with your merged work.

---

### 📋 Full Checklist Summary

| Step | Command | Purpose |
|:-----|:--------|:--------|
| Check branch | `git branch` | See where you are |
| Checkout main | `git checkout main` | Go to main |
| Pull latest main | `git pull origin main` | Update main |
| Create new branch | `git checkout -b add-footer` | New feature branch |
| Stage changes | `git add .` | Select files |
| Commit changes | `git commit -m "message"` | Save changes locally |
| Push new branch | `git push -u origin add-footer` | Upload branch to GitHub |
| Checkout main again | `git checkout main` | Switch back |
| Pull latest main again | `git pull origin main` | Stay updated |
| Merge feature branch | `git merge add-footer` | Combine work |
| Push updated main | `git push origin main` | Final upload |

