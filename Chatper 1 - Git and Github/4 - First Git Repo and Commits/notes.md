
# First Git Repository and Commits

## Initializing a New Git Repository

Here, we are going to initialize a new Git repository.

We can initialize a Git repository in two ways:

1. **Using GUI:** Initialize a repository through the Source Control panel in Visual Studio Code.
2. **Using CLI:** Initialize a repository using Git commands in the terminal.

## Git Commands – Step by Step

### 1. Initialize a Git Repository

```bash
git init
```

- Initializes a new Git repository in the current folder.
- Creates a hidden `.git` directory.
- Git starts tracking the repository's version history.

### 2. Add Files to the Staging Area

```bash
git add .
```

- Adds all new and modified files in the current directory to the staging area.
- The staging area contains the changes that are ready to be included in the next commit.
- These changes will be included in the repository's next commit.
- It does not create a commit yet.

### 3. Check the Repository Status

```bash
git status
```

- Displays the current status of the working directory and staging area.
- Shows which files are modified, untracked, or staged.
- Helps us understand which changes are ready to be committed.

### 4. Commit the Changes

```bash
git commit -m "Initial commit"
```

- Saves the staged changes as a new commit in the repository.
- Records a snapshot of the project at that point.
- The commit message describes the changes made.
- Every commit has a unique identifier called a commit hash.

### 5. View Commit History

```bash
git log
```

- Displays the commit history of the current branch.
- Shows the commit hash, author, date, and commit message.
- Helps us track previous changes.

```bash
git log --oneline
```

- Displays commit history in a compact, single-line format.

### 6. Check the Current Branch

```bash
git branch
```

- Displays all local branches.
- Shows the currently active branch with an asterisk (`*`).

### 7. Create a New Branch

```bash
git branch feature/login
```

- Creates a new branch named `feature/login`.
- The new branch starts from the current commit.
- It does not automatically switch to the newly created branch.

### 8. Switch to Another Branch

```bash
git checkout feature/login
```

- Switches to the specified branch.
- Updates the working directory to match that branch.

**Alternative modern command:**

```bash
git switch feature/login
```

### 9. Create and Switch to a New Branch

```bash
git checkout -b feature/signup
```

- Creates a new branch named `feature/signup`.
- Automatically switches to the newly created branch.

**Alternative modern command:**

```bash
git switch -c feature/signup
```

### 10. View File Changes

```bash
git diff
```

- Shows the differences between the working directory and the staging area.
- Helps us identify what changes have been made but not yet staged.

```bash
git diff --staged
```

- Shows the differences between the staged changes and the latest commit.

### 11. Remove Files from the Staging Area

```bash
git restore --staged filename
```

- Removes the specified file from the staging area.
- Keeps the changes in the working directory.
- Does not delete the file.

### 12. Push Changes to GitHub

```bash
git push origin main
```

- Uploads local commits from the `main` branch to the remote repository on GitHub.
- `origin` represents the remote repository's default name.
- `main` specifies the branch to push.

### 13. Pull Changes from GitHub

```bash
git pull origin main
```

- Fetches the latest changes from the remote `main` branch.
- Integrates those changes into the current local branch.

### 14. Clone a Repository

```bash
git clone <repository-url>
```

- Downloads a remote Git repository to your local computer.
- Creates a local copy of the repository, including its commit history.
- Automatically configures the remote repository.

### 15. Merge Branches

```bash
git merge feature/login
```

- Merges the changes from the `feature/login` branch into the currently checked-out branch.
- Combines the development work from different branches.

### 16. Delete a Local Branch

```bash
git branch -d feature/login
```

- Deletes the specified local branch.
- Usually allows deletion only when the branch has been fully merged.

### 17. Connect a Local Repository to GitHub

```bash
git remote add origin <repository-url>
```

- Connects the local Git repository to a remote repository on GitHub.
- `origin` is the conventional name given to the remote repository.

### 18. View Remote Repositories

```bash
git remote -v
```

- Displays the configured remote repositories.
- Shows the URLs used for fetching and pushing changes.

