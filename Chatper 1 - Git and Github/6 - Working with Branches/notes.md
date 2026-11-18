# Working with Git Branches

Git branches allow developers to work on different features, bug fixes, or tasks independently without directly affecting the main project branch.

## 1. List Existing Branches

Display all local branches:

```bash
git branch
```

Display both local and remote branches:

```bash
git branch -a
```

## 2. Create a New Branch

Create a branch without switching to it:

```bash
git branch feature/login
```

Create a branch and switch to it:

```bash
git switch -c feature/login
```

## 3. Switch Between Branches

Switch to an existing branch:

```bash
git switch main
```

Switch to another branch:

```bash
git switch feature/login
```

## 4. Create a Branch Based on Another Branch

First, switch to the branch you want to use as the starting point:

```bash
git switch development
```

Get the latest changes from the remote branch:

```bash
git pull origin development
```

Create a new branch based on the current `development` branch:

```bash
git switch -c feature/signup
```

Now, `feature/signup` is based on the latest commit of your local `development` branch.

## 5. Rename a Branch

Rename the current branch:

```bash
git branch -m feature/login
```

Rename another local branch:

```bash
git branch -m old-branch-name new-branch-name
```

## 6. Delete a Branch

Delete a local branch that has been merged:

```bash
git branch -d feature/login
```

Force-delete a local branch:

```bash
git branch -D feature/login
```

Delete a remote branch:

```bash
git push origin --delete feature/login
```

**Note:** You cannot delete the branch you are currently working on. Switch to another branch first.

## 7. Push a New Branch to GitHub

Push the branch and set its upstream tracking branch:

```bash
git push -u origin feature/login
```

After setting the upstream, you can simply use:

```bash
git push
```

## 8. Merge One Branch into Another

Suppose you want to merge `feature/login` into `development`.

First, switch to the target branch:

```bash
git switch development
```

Merge the feature branch:

```bash
git merge feature/login
```

Now, the changes from `feature/login` are merged into `development`.

## 9. Get the Latest Changes from a Remote Branch

```bash
git pull origin development
```

This fetches and integrates the latest changes from the remote `development` branch into your current local branch.

## 10. View Branch Information

View the current branch:

```bash
git branch --show-current
```

View branches with their latest commits:

```bash
git branch -v
```

View the commit history of all branches:

```bash
git log --oneline --all --graph
```

---

## Practical Example: Working with Feature Branches

Suppose your team has a `development` branch, and you need to work on a login feature.

```bash
# 1. Switch to development
git switch development

# 2. Get the latest changes
git pull origin development

# 3. Create a new feature branch
git switch -c feature/login

# 4. Check the current branch
git branch

# 5. Stage your changes
git add .

# 6. Commit your changes
git commit -m "Added login feature"

# 7. Push your branch to GitHub
git push -u origin feature/login
```

After pushing, you can create a Pull Request to merge `feature/login` into `development`.

## Important Git Branch Commands

| Command | Purpose |
|---|---|
| `git branch` | List local branches |
| `git branch -a` | List all branches |
| `git branch branch-name` | Create a branch |
| `git switch branch-name` | Switch branches |
| `git switch -c branch-name` | Create and switch |
| `git branch -m new-name` | Rename current branch |
| `git branch -d branch-name` | Delete local branch |
| `git merge branch-name` | Merge a branch |
| `git push -u origin branch-name` | Push a new branch |
| `git pull origin branch-name` | Pull remote changes |

## Important Points to Remember

- A branch allows you to work independently without directly changing another branch.
- Always check your current branch before making changes.
- Create feature branches from the correct base branch, such as `main` or `development`.
- Commit your changes before switching branches to avoid carrying unwanted uncommitted changes.
- Push your feature branch to GitHub when you want to share your work.
- Use Pull Requests to review and merge changes into the target branch.

**Remember:** Use `git branch` or `git status` to check which branch you are currently working on.