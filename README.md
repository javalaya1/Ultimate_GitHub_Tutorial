# Git & GitHub Tutorial

---
### Day-01 : https://youtu.be/ERTz8EkHBBA
### Day-02 : https://youtu.be/MVq5TORaIC0
### Day-03 : https://youtu.be/nNkV1Q3NDt0
### Day-04 : https://youtu.be/ee5sNe6G6SQ
---

## Git & GitHub Class Notes

- **Git** is a version control software.
- **GitHub** is a platform used to store all developers' project source code in one place.
- On GitHub, we can create repositories to store project code.
- All developers can connect to the GitHub repository for code integration (making code integration very easy).
- GitHub allows tracking of all code changes:
  - Who modified
  - When modified
  - What was modified
  - Why modified

---

## Environment Setup

1. Create an account at [github.com](https://www.github.com) (free of cost).
2. Download & install Git client software: [https://git-scm.com/downloads](https://git-scm.com/downloads)
3. Open Git Bash and configure your name and email:
   ```bash
   git config --global user.name "your-name"
   git config --global user.email "your-email"
   ```

> Configuring name and email is a one-time process.

---

## What is a GitHub Repository?

- A repository is a place to store project source code/files.
- For each project, one GitHub repository is created.
- Two types of repositories:
  1. **Public Repo**: Anybody can see & you choose who can commit.
  2. **Private Repo**: You choose who can see & who can commit.

### Example:
Project Git Repo URL: `https://github.com/ashokitschool/sbi_loans_app.git`

Project team members use the repo URL to connect.

---

## Git Architecture

1. Working Tree
2. Staging Area
3. Local Repository
4. Central Repository (Remote)

---
![Project Screenshot](git-architecture.gif)
---

## Git Bash Commands

```bash
git init              # Initialize working tree
git status            # Show working tree status
git add <file-name>   # Add file to staging area
git add .             # Add all files to staging area
git commit -m "msg"   # Commit staged files to local repo
git push              # Push local commits to remote repo
git restore <file>    # Unstage or discard changes
git log               # Show commit history
git rm <file-name>    # Remove a file
git clone <repo-url>  # Download remote repo to local
git pull              # Get latest changes from remote repo
```

> Note: After `git rm`, commit and push to delete file from remote repo.

---

## Git GUI

- A desktop tool to perform Git operations.
- Run in working tree:

```bash
git gui
```

---

## .gitignore File

- Specifies files/folders to skip in Git operations.

### Example:
```
.settings
.classpath
.project
target/
```

---

## Git Branches

When multiple teams work on the same repo, use branches to avoid delivery issues.

### Recommended Branches:

- `main` (default)
- `develop` (development team)
- `sit` (bug fixing team)
- `research` (R&D team)
- `release` (production team)

> Multiple teams can work in parallel using branches.

---

## Lab Task

1. Go to GitHub and create `develop` branch from `main`.
2. Clone the repo (main branch will be cloned by default):
   ```bash
   git clone <url>
   ```
3. Switch to develop branch:
   ```bash
   git checkout develop
   ```
4. Create a file and push it to `develop` branch.
5. Create a Pull Request and merge `develop` into `main`.

---

# Git Interview Concepts

---

## ✅ What is a Pull Request?

A **Pull Request** is used to merge changes from one branch into another.

**Example:**  
Merging changes from the `develop` branch to the `main` branch.

---

## ✅ What is Git Stash?

**Git Stash** is used to save the current changes in a backup (stash) and make the working directory clean.

### Example Scenario:

- `JIRA-101` assigned at 9 AM → Work started, partial changes done.
- At 11 AM, `JIRA-102` assigned → It's critical.
- To work on `JIRA-102`, stash the `JIRA-101` changes:
  
  ```bash
  git stash
  ```

- After pushing `JIRA-102` changes, get `JIRA-101` changes back to working tree :
  
  ```bash
  git stash apply
 ```

---

## ✅ How to Remove Git Local Commits?

Use the `git reset` command to undo local commits.

### Types of Reset:

- **Soft Reset**: Removes commit but retains changes in the staging area.
  
  ```bash
  git reset --soft HEAD~1
  ```

- **Hard Reset**: Removes both commit and file changes.
  
  ```bash
  git reset --hard HEAD~1
  ```

---

## ✅ How to Revert Central Repo Commits?

Use the `git revert` command to undo changes from the remote repository.

```bash
git revert <commit-id>
git push
```

---

## ✅ What is Git Cherry-pick?

- By default, `git merge` merges all commits from one branch to another.
- If you want to merge only a **specific commit**, use `git cherry-pick`.

```bash
git cherry-pick <commit-id>
```

---

## ✅ Git Pull vs Git Fetch

| Command     | Description                                                |
|-------------|------------------------------------------------------------|
| `git pull`  | Downloads changes from the remote repo and merges into working directory |
| `git fetch` | Downloads changes to the local repo only                   |

To merge after `fetch`, run:

```bash
git merge
```

> `git pull` = `git fetch` + `git merge`

---

## ✅ What is Git Fork?

**Git Fork** is used to copy someone else's GitHub repository into your own GitHub account.
so open other's public git repository, click on fork available in their central repository, it will divert the project to our account as you are the owner, you can change the name or no need to edit that name field.

click on green color "Create fork" button to confirm

- Useful for contributing to open-source projects.
---

Collaboration:



---
