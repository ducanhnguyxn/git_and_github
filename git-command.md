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
# 17. Undo Changes ↩️

### Unstage a file but keep the changes:

```bash
git restore --staged filename.txt
```

### Discard changes in one file:

```bash
git restore filename.txt
```

⚠️ This will permanently remove your uncommitted changes.

### Discard all changes:

```bash
git restore .
```

### Undo the last commit but keep your changes:

```bash
git reset --soft HEAD~1
```

### Undo the last commit and unstage the changes:

```bash
git reset HEAD~1
```

### Completely remove the last commit and changes:

```bash
git reset --hard HEAD~1
```

⚠️ Be careful with `--hard` because deleted changes can be difficult to recover.

---

# 18. Git Stash 📦

Use Git stash when you want to temporarily save your changes without committing them.

### Save your current changes:

```bash
git stash
```

### See all saved stashes:

```bash
git stash list
```

### Apply the latest stash:

```bash
git stash apply
```

### Apply and remove the latest stash:

```bash
git stash pop
```

### Apply a specific stash:

```bash
git stash apply stash@{0}
```

### Delete a specific stash:

```bash
git stash drop stash@{0}
```

### Delete all stashes:

```bash
git stash clear
```

---

# 19. Git Tags 🏷️

Tags are usually used to mark versions of your project.

### Create a tag:

```bash
git tag v1.0.0
```

### Create an annotated tag:

```bash
git tag -a v1.0.0 -m "Version 1.0.0"
```

### See all tags:

```bash
git tag
```

### Push one tag to GitHub:

```bash
git push origin v1.0.0
```

### Push all tags:

```bash
git push origin --tags
```

---

# 20. Git Ignore 🚫

Create a file called:

```text
.gitignore
```

Use it to stop Git from tracking files or folders you don't want to upload.

Example `.gitignore`:

```text
# Dependencies
node_modules/

# Environment variables
.env

# System files
.DS_Store

# Build files
dist/

# Log files
*.log
```

After creating it:

```bash
git add .gitignore
git commit -m "Add gitignore"
git push
```

---

# 21. View Git History 📖

### Normal history:

```bash
git log
```

### Short history:

```bash
git log --oneline
```

### See a visual branch history:

```bash
git log --oneline --graph --decorate --all
```

### See changes from a specific commit:

```bash
git show COMMIT_ID
```

Example:

```bash
git show abc123
```

### See the history of one file:

```bash
git log -- filename.txt
```

---

# 22. Working With Remotes 🌍

### Check your remote repositories:

```bash
git remote -v
```

### Add a remote:

```bash
git remote add origin REPOSITORY_URL
```

### Change a remote URL:

```bash
git remote set-url origin NEW_REPOSITORY_URL
```

### Remove a remote:

```bash
git remote remove origin
```

### Download changes without merging them:

```bash
git fetch
```

### See remote branches:

```bash
git branch -r
```

---

# 23. Git Aliases ⚡

Aliases allow you to create shortcuts for Git commands.

### Check existing aliases:

```bash
git config --global --get-regexp alias
```

### Create a shortcut for `git status`:

```bash
git config --global alias.st status
```

Now you can type:

```bash
git st
```

### Useful aliases:

```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.last "log -1 HEAD"
```

Create a shortcut for a nice Git history:

```bash
git config --global alias.graph "log --oneline --graph --decorate --all"
```

Then use:

```bash
git graph
```

---

# 24. Useful Advanced Commands 🚀

### Find a bug using Git Bisect:

```bash
git bisect start
```

### See where HEAD has been:

```bash
git reflog
```

This can help recover commits that you accidentally lost.

### Remove untracked files:

```bash
git clean -fd
```

⚠️ Be careful. This permanently deletes untracked files and folders.

### Check repository size and objects:

```bash
git count-objects -vH
```

### Check repository integrity:

```bash
git fsck
```

---

# 25. Common Git Workflows 🔗

## Basic Feature Branch Workflow

Create a new branch:

```bash
git switch -c feature-name
```

Make your changes, then:

```bash
git add .
git commit -m "Add new feature"
```

Push the branch:

```bash
git push -u origin feature-name
```

Then create a Pull Request on GitHub.

---

## Keep Your Project Up to Date

Before starting work:

```bash
git pull
```

Or:

```bash
git fetch
git merge origin/main
```

---

## Fork and Pull Request Workflow

1. Fork the repository on GitHub.
2. Clone your fork:

```bash
git clone YOUR_FORK_URL
```

3. Create a branch:

```bash
git switch -c feature-name
```

4. Make your changes.
5. Add and commit:

```bash
git add .
git commit -m "Describe your changes"
```

6. Push your branch:

```bash
git push origin feature-name
```

7. Create a Pull Request on GitHub.

---

# 26. Good Commit Messages ✍️

Try to make your commit messages clear.

### Good examples:

```bash
git commit -m "Add user login page"
```

```bash
git commit -m "Fix navigation bug"
```

```bash
git commit -m "Update README instructions"
```

### Avoid messages like:

```text
update
fix
asdf
changes
```

A good commit message should explain **what changed**.

---

# 27. My Most Used Git Commands 🔥

This is the workflow you will probably use the most:

```bash
git status
```

⬇️

```bash
git add .
```

⬇️

```bash
git commit -m "Describe what you changed"
```

⬇️

```bash
git push
```

## Remember:

```text
git add = prepare changes
git commit = save changes
git push = upload changes to GitHub
```

🔥 **The basic Git workflow:**

```bash
git status
git add .
git commit -m "your message"
git push
```

# Bonus: Before You Push Checklist

* [ ] Check your changes with `git status`
* [ ] Review your code
* [ ] Make sure you are on the correct branch
* [ ] Run `git add .`
* [ ] Write a meaningful commit message
* [ ] Push with `git push`
* [ ] Check GitHub to make sure your changes were uploaded

