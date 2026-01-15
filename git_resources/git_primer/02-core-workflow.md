# The Core Git Workflow

This is basic workflow you will use the vast majority of the time you are using git. 

## 1. Check status
```bash
git status
```

Always start here. To explain what outputs you might see when running this, let's look at an example output: 

```bash
On branch feature/user-auth 
Your branch is ahead of 'origin/feature/user-auth' by 1 commit. 
  (use "git push" to publish your local commits)

Your branch is behind 'origin/feature/user-auth' by 2 commits.
  (use "git pull" to update your local branch)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   src/auth/login.py
        new file:   src/auth/session.py
        deleted:    src/auth/legacy_auth.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   src/auth/login.py
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        notes/debugging.txt
        tmp/test_output.json

```
We will run through this line by line. 

```bash
On branch feature/user-auth 
```

This tells you what 