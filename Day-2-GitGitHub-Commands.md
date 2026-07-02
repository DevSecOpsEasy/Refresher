# Day 1 -- Git & GitHub Commands

## Learning Objectives

By the end of this session, you will be able to:

-   Understand what Git is and why it is used.
-   Understand the difference between Git and GitHub.
-   Create and manage a local Git repository.
-   Track changes using commits.
-   Work with branches.
-   Connect a local repository to GitHub.
-   Push and pull code from a remote repository.

------------------------------------------------------------------------

# Git vs GitHub

  Git                           GitHub
  ----------------------------- ---------------------------------------------
  Version Control System        Cloud platform for hosting Git repositories
  Works on your local machine   Stores repositories online
  Tracks code changes           Enables collaboration

**Remember:** - **Git** = Tool - **GitHub** = Website that hosts Git
repositories

------------------------------------------------------------------------

# Git Workflow

``` text
Working Directory
       │
       ▼
 git add
       │
       ▼
Staging Area
       │
       ▼
git commit
       │
       ▼
Local Repository
       │
       ▼
git push
       │
       ▼
GitHub Repository
```

------------------------------------------------------------------------

# 1. Check Git Installation

``` bash
git --version
```

------------------------------------------------------------------------

# 2. Configure Git

``` bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list
```

> Configure Git only once on a new computer.

------------------------------------------------------------------------

# 3. Create a Repository

``` bash
mkdir git-demo
cd git-demo
git init
```

Check repository status:

``` bash
git status
```

------------------------------------------------------------------------

# 4. Create Files

``` bash
touch README.md
touch app.py
echo "# My First Project" > README.md
```

------------------------------------------------------------------------

# 5. Stage Files

Single file

``` bash
git add README.md
```

Multiple files

``` bash
git add README.md app.py
```

Everything

``` bash
git add .
```

------------------------------------------------------------------------

# 6. Commit Changes

``` bash
git commit -m "Initial commit"
git commit -m "Added README"
git commit -m "Updated application"
```

**Good commit messages are short and meaningful.**

Examples: - Fixed login bug - Added Dockerfile - Updated documentation

------------------------------------------------------------------------

# 7. Check Repository Status

``` bash
git status
```

This is the most frequently used Git command.

------------------------------------------------------------------------

# 8. View History

``` bash
git log
git log --oneline
git log --graph
git log --stat
```

------------------------------------------------------------------------

# 9. View Differences

``` bash
git diff
git diff --staged
```

------------------------------------------------------------------------

# 10. Restore Changes

Discard local changes

``` bash
git restore README.md
```

Unstage a file

``` bash
git restore --staged README.md
```

------------------------------------------------------------------------

# 11. Rename and Delete Files

``` bash
git mv old.txt new.txt
git rm file.txt
```

Commit afterwards:

``` bash
git commit -m "Renamed file"
```

------------------------------------------------------------------------

# 12. Ignore Files

Create a .gitignore file.

Example:

``` text
*.log
*.class
.env
node_modules/
target/
```

------------------------------------------------------------------------

# 13. Branching

View branches

``` bash
git branch
```

Create

``` bash
git branch dev
```

Switch

``` bash
git switch dev
```

Create & switch

``` bash
git switch -c feature/login
```

------------------------------------------------------------------------

# 14. Merge

``` bash
git switch main
git merge dev
```

------------------------------------------------------------------------

# 15. Delete Branch

``` bash
git branch -d dev
git branch -D dev
```

------------------------------------------------------------------------

# 16. Clone Repository

``` bash
git clone https://github.com/username/repository.git
```

------------------------------------------------------------------------

# 17. Remote Repository

``` bash
git remote -v
git remote add origin https://github.com/username/repository.git
git remote remove origin
```

------------------------------------------------------------------------

# 18. Push Code

First push

``` bash
git push -u origin main
```

Future pushes

``` bash
git push
```

------------------------------------------------------------------------

# 19. Get Latest Changes

``` bash
git pull
git fetch
git fetch --all
```

**Difference**

-   `git fetch` downloads changes only.
-   `git pull` downloads and merges changes.

------------------------------------------------------------------------

# 20. Tags

``` bash
git tag
git tag v1.0
git push origin v1.0
```

------------------------------------------------------------------------

# 21. Stash

``` bash
git stash
git stash list
git stash pop
git stash apply
```

------------------------------------------------------------------------

# 22. Undo Commits

``` bash
git reset --soft HEAD~1
git reset --mixed HEAD~1
git reset --hard HEAD~1
```

------------------------------------------------------------------------

# 23. Useful Commands

``` bash
git show
git reflog
git blame README.md
git ls-files
```

------------------------------------------------------------------------

# GitHub Basics

## Create a Repository

1.  Sign in to GitHub.
2.  Click **New Repository**.
3.  Enter a repository name.
4.  Choose Public or Private.
5.  Click **Create Repository**.

## Connect Local Repository

``` bash
git remote add origin https://github.com/username/repository.git
```

## Push Existing Project

``` bash
git branch -M main
git push -u origin main
```

------------------------------------------------------------------------

# Daily Git Workflow

``` bash
git pull
git switch -c feature/new-feature

# Make changes

git status
git add .
git commit -m "Implemented feature"

git push -u origin feature/new-feature
```

------------------------------------------------------------------------

# Hands-on Lab

``` bash
mkdir git-lab
cd git-lab

git init

git config user.name "Student"
git config user.email "student@example.com"

echo "# DevOps" > README.md

git status

git add .
git commit -m "Initial commit"

git branch dev
git switch dev

echo "Git Practice" >> README.md

git add README.md
git commit -m "Updated README"

git switch main
git merge dev

git log --oneline --graph

git branch -d dev
```

------------------------------------------------------------------------

# Best Practices

-   Commit small and frequently.
-   Write meaningful commit messages.
-   Pull before starting work.
-   Never commit passwords or secrets.
-   Use `.gitignore` for unnecessary files.
-   Create feature branches for new work.
-   Test your code before pushing.

------------------------------------------------------------------------

# Summary

Git is the industry-standard version control system. Every DevOps,
Cloud, SRE, Platform, and Software Engineer uses Git daily. Mastering
these commands will make collaboration easier and prepare you for
real-world projects.
