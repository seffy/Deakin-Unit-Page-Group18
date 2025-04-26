# 📋 Best Practices for Team Leaders Managing Git Updates

## 1. 🔍 Check for New Updates Regularly
- Run `git fetch origin` daily or before starting work.
- Check remote branches using `git branch -r`.
- Review GitHub Pull Requests if available.

## 2. 📥 Pull Updates into Local Main Safely
```bash
git checkout main
git pull origin main
```
✅ Always pull the latest changes before merging new work.

## 3. 🔀 Merge Developer Branches One by One
```bash
git merge origin/branch-name
```
Example:
```bash
git merge origin/add-footer
git merge origin/add-header
```
✅ Resolve any merge conflicts.

## 4. 🔎 Test the Project After Merging
- Open the project locally.
- Check that all merged updates work correctly.

## 5. 📤 Push the Updated Main Back to GitHub
```bash
git push origin main
```
✅ Push the final combined version to GitHub.

## 6. 🧹 Delete Feature Branches (Optional but Recommended)
Delete locally:
```bash
git branch -d branch-name
```
Delete remotely:
```bash
git push origin --delete branch-name
```
✅ Keeps the GitHub repository clean.

## 7. 💬 Communicate with Developers
Inform the team:
> "Main branch updated — please pull the latest version before starting new work."

## 8. 📋 Maintain a Merge Log (Optional)
| Date | Branch | Merged by | Notes |
|:-----|:-------|:----------|:------|
| 20 May | add-footer | Joseph | Footer section merged |
| 21 May | add-header | Joseph | Header UI updates merged |

---

# 🧠 Leadership Tips
| Tip | Why |
|:----|:----|
| Merge often | Prevent large conflicts |
| Communicate clearly | Keep everyone updated |
| Test after merging | Ensure project quality |
| Clean up branches | Keep the repo organized |

---

# 🚀 Final Git Workflow for Team Leader

```bash
git fetch origin
git checkout main
git pull origin main
git merge origin/developer-branch
git test the project locally
git push origin main
(optional) git branch -d developer-branch
(optional) git push origin --delete developer-branch
```

✅ Repeat for each developer update to keep the project flowing smoothly!

