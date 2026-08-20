# Git Commands Notebook 📘

## 1. Check Git Version

```bash
git --version
```

---

# 2. Configure Git

Set your username:

```bash
git config --global user.name "Your Name"
```

Set your email:

```bash
git config --global user.email "your@email.com"
```

Check your configuration:

```bash
git config --list
```

---

# 3. Start a Git Repository

Go into your project folder:

```powershell
cd path\to\your\folder
```

Example:

```powershell
cd D:\learngit\gitone
```

Initialize Git:

```bash
git init
```

Check the repository status:

```bash
git status
```

---

# 4. Add Files

Add one specific file:

```bash
git add filename.txt
```

Example:

```bash
git add README.md
```

Add all files:

```bash
git add .
```

Check what will be committed:

```bash
git status
```

---

# 5. Commit Changes

Create a commit:

```bash
git commit -m "Your commit message"
```

Example:

```bash
git commit -m "Add README file"
```

Check commit history:

```bash
git log
```

Short version:

```bash
git log --oneline
```

---

# 6. Connect Your Project to GitHub

Add your GitHub repository:

```bash
git remote add origin YOUR_REPOSITORY_URL
```

Check the remote:

```bash
git remote -v
```

Example:

```bash
git remote add origin https://github.com/username/repository.git
```

---

# 7. Push Your Project to GitHub

Rename your branch to `main`:

```bash
git branch -M main
```

Push for the first time:

```bash
git push -u origin main
```

After that, you can usually just use:

```bash
git push
```

---

# 8. Normal Workflow 🔥

This is the workflow you will use most of the time:

```bash
git status
```

```bash
git add .
```

```bash
git commit -m "Describe what you changed"
```

```bash
git push
```

### Quick version:

```bash
git add .
git commit -m "Update project"
git push
```

---

# 9. Check Changes

See the status:

```bash
git status
```

See changes before adding:

```bash
git diff
```

See commit history:

```bash
git log --oneline
```

---

# 10. Create a New Branch

Create a branch:

```bash
git branch branch-name
```

Switch to a branch:

```bash
git switch branch-name
```

Create and switch at the same time:

```bash
git switch -c branch-name
```

Check branches:

```bash
git branch
```

---

# 11. Merge a Branch

Switch to `main`:

```bash
git switch main
```

Merge another branch:

```bash
git merge branch-name
```

---

# 12. Download Changes From GitHub

Get the latest changes:

```bash
git pull
```

Or:

```bash
git pull origin main
```

---

# 13. Clone a Repository

Download an existing GitHub repository:

```bash
git clone REPOSITORY_URL
```

Example:

```bash
git clone https://github.com/username/repository.git
```

---

# 14. Remove a File From Git

Remove a file:

```bash
git rm filename.txt
```

Then commit and push:

```bash
git commit -m "Remove file"
git push
```

---

# 15. Rename a File

```bash
git mv oldname.txt newname.txt
```

Then:

```bash
git commit -m "Rename file"
git push
```

---

# 16. Useful Commands Cheat Sheet

| Command                     | What it does             |
| --------------------------- | ------------------------ |
| `git init`                  | Start a Git repository   |
| `git status`                | Check file status        |
| `git add .`                 | Add all files            |
| `git add filename`          | Add one file             |
| `git commit -m "message"`   | Save changes             |
| `git log`                   | View commit history      |
| `git log --oneline`         | Short commit history     |
| `git branch`                | View branches            |
| `git switch branch-name`    | Switch branch            |
| `git switch -c branch-name` | Create and switch branch |
| `git merge branch-name`     | Merge a branch           |
| `git remote -v`             | Check GitHub connection  |
| `git pull`                  | Download latest changes  |
| `git push`                  | Upload changes to GitHub |
| `git clone URL`             | Download a repository    |

---

# My Most Used Commands 🚀

```bash
git status
git add .
git commit -m "your message"
git push
```

### Remember:

**`git add` → `git commit` → `git push`**

1. `git add .` = Prepare your changes
2. `git commit -m "message"` = Save your changes
3. `git push` = Upload to GitHub
