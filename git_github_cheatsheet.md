# Git & GitHub Cheat Sheet

A quick reference for the most useful Git & GitHub commands.

---

## Configuration
```
git config --global user.name "Your Name"         # Set username
git config --global user.email "you@example.com"  # Set email
git config --global core.editor "code --wait"     # Set default editor (VS Code)
git config --global init.defaultBranch main       # Set default branch name
git config --list                                 # Show all configs
```

---

## Start a Repository
```
git init                  # Start a new repository
git clone <url>           # Clone from GitHub
```

---

## Daily Workflow
```
git status                # Check status of files
git add <file>            # Stage a file
git add .                 # Stage all changes
git commit -m "message"   # Commit with message
git push                  # Push changes to remote
git pull                  # Pull latest changes from remote
```

---

## Branching & Merging
```
git branch                # List branches
git branch <name>         # Create new branch
git checkout <name>       # Switch branch
git checkout -b <name>    # Create & switch to branch
git merge <branch>        # Merge branch into current
git rebase <branch>       # Reapply commits on top of another branch
git branch -d <name>      # Delete branch
```

---

## Undo & Fix
```
git restore <file>        # Discard changes in working dir
git reset <file>          # Unstage a file
git reset --soft HEAD~1   # Undo last commit (keep changes staged)
git reset --hard HEAD     # Reset to last commit (⚠️ discards changes)
git commit --amend        # Edit last commit message / add changes
```

---

## Logs & History
```
git log                   # Show commit history
git log --oneline         # Compact log view
git show <commit>         # Show details of a commit
git reflog                # Show all refs (great for recovery)
```

---

## Remote Repositories
```
git remote -v             # Show remote repos
git remote add origin <url>  # Add remote repo
git push -u origin main   # Push branch for the first time
git fetch                 # Fetch updates (no merge)
git pull                  # Fetch + merge
```

---

## Stash (Save Work Temporarily)
```
git stash                 # Stash changes
git stash list            # Show stashes
git stash pop             # Reapply & drop last stash
git stash apply           # Reapply stash (keep it saved)
```

---

## Tags & Releases
```
git tag                   # List tags
git tag <name>            # Create tag
git push origin <tag>     # Push tag to remote
```

---

## GitHub Workflow (Contributing)
1. Fork repository (if not yours)
2. Clone repository locally
3. Create feature branch (`git checkout -b feature-xyz`)
4. Make changes & commit
5. Push branch to GitHub
6. Create Pull Request (PR)
7. Review & merge

---

## Pro Tips
- Use `.gitignore` to skip files/folders
- Use `git stash` to save work in progress
- Use `git rebase` to keep history clean
- Use `git reflog` to recover lost commits
