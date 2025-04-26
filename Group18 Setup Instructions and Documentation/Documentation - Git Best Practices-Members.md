# 📋 Best Practices for Team Members (Git + GitHub)

## ✅ 1. Start Every Work Session by Updating Main
```bash
git checkout main
git pull origin main
```
✅ Always work with the latest version.

---

## ✅ 2. Create a New Feature Branch
```bash
git checkout -b your-feature-branch
```
Example:
```bash
git checkout -b add-footer
```
✅ Isolate your changes safely.

---

## ✅ 3. Make Changes Locally
- Edit assigned files (HTML, CSS, JS, etc.)
- Save changes properly.

---

## ✅ 4. Stage and Commit Your Changes
```bash
git add .
git commit -m "Short clear message (e.g., Update footer section)"
```
✅ Save your progress in Git.

---

## ✅ 5. Push Your Branch to GitHub
For the first push:
```bash
git push -u origin your-feature-branch
```
Afterward:
```bash
git push
```
✅ Send your work to GitHub.

---

## ✅ 6. Notify the Team Leader
Send a quick message like:
> "Hi, I finished updating `add-footer` branch. It's ready for merging!"

---

## ✅ 7. Wait for Merge and Pull Again
After merging:
```bash
git checkout main
git pull origin main
```
✅ Always update before starting new work.

---

# 📋 Summary Checklist

| Step | Command |
|:-----|:--------|
| Update main | `git pull origin main` |
| Create branch | `git checkout -b branch-name` |
| Stage files | `git add .` |
| Commit work | `git commit -m "message"` |
| Push branch | `git push -u origin branch-name` |
| Notify Team Lead | Quick message |
| Pull after merging | `git pull origin main` |

---

# 📢 Important Tips for Team Members

| Tip | Why |
|:----|:----|
| Always pull first | Prevent outdated work |
| Never edit directly on main | Avoid conflicts |
| Communicate when done | Keep merges organized |
| Keep commits small and clear | Easier tracking |

