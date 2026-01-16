# Resolving (Merge) Conflicts

When you merge branches, there is a good chance that you will run into a message like this: 

```bash
git merge feature/user-auth
Auto-merging src/auth/login.py
CONFLICT (content): Merge conflict in src/auth/login.py
```

What does this mean? This implies that in the `login.py` file, there is a difference in the code in our local branch and the remote branch. Note that the only differences that matter is that when code on one line in the file on one branch is different than the code on that same line in the file on the other branch. To be more specific, if I added new lines of code, there is no merge conflict. However, if I change an existing line of code, there is an issue. 

In this hypothetical example, say I open up `login.py`:

```python
def login(user, password):
<<<<<<< HEAD
    if not user.is_active:
        raise PermissionError("User account is inactive")
    token = generate_token(user)
    return token
=======
    token = generate_token(user)
    log_login_attempt(user)
    return token
>>>>>>> feature/user-auth
```

