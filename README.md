# Git & GitHub – DevOps Learning Notes

A quick reference guide covering the Git and GitHub concepts and commands I learned during my DevOps learning journey.

---

# 1. Git Workflow

Git follows a basic workflow:

```text
Working Directory
        ↓
Staging Area
        ↓
Local Repository
        ↓
Remote Repository
        ↓
GitHub
```

---

## Working Directory

The **Working Directory** is the location where we create and modify files.

```text
Working Directory
       ↓
Create / Modify Files
```

---

## Staging Area

The **Staging Area** is where we prepare changes before committing them.

Command:

```bash
git add .
```

Flow:

```text
Modified Files
      ↓
git add
      ↓
Staging Area
```

---

## Local Repository

The **Local Repository** is the Git repository stored on our local machine.

Command:

```bash
git commit -m "message"
```

Flow:

```text
Staging Area
      ↓
git commit
      ↓
Local Repository
```

---

## Remote Repository

A **Remote Repository** is a Git repository hosted on a remote platform such as GitHub.

Flow:

```text
Local Repository
       ↓
    git push
       ↓
GitHub Repository
```

---

# 2. Git Configuration

Check Git version:

```bash
git --version
```

Configure username:

```bash
git config --global user.name "Your Name"
```

Configure email:

```bash
git config --global user.email "your@email.com"
```

View Git configuration:

```bash
git config --list
```

---

# 3. Create a Git Repository

Create a project directory:

```bash
mkdir gitproject
```

Move into the directory:

```bash
cd gitproject
```

Initialize Git:

```bash
git init
```

Check repository status:

```bash
git status
```

Workflow:

```text
Create Directory
       ↓
     git init
       ↓
Git Repository
       ↓
   git status
```

---

# 4. Basic Git Commands

## Add a Single File

```bash
git add filename
```

---

## Add All Files

```bash
git add .
```

---

## Commit Changes

```bash
git commit -m "Initial commit"
```

A commit records the staged changes in the local Git repository.

---

## View Commit History

```bash
git log
```

---

## View Changes

```bash
git diff
```

---

# 5. Git Status

Check the current state of the repository:

```bash
git status
```

It can show:

```text
Modified Files
Untracked Files
Staged Files
Branch Information
```

Example workflow:

```text
Working Directory
       ↓
   git status
       ↓
Check Changes
       ↓
   git add .
       ↓
   git commit
```

---

# 6. Connect Git to GitHub

Add a remote repository:

```bash
git remote add origin <repository-url>
```

Check the configured remote:

```bash
git remote -v
```

---

## Rename Branch to Main

```bash
git branch -M main
```

---

## Push Code to GitHub

```bash
git push -u origin main
```

Complete flow:

```text
Local Project
     ↓
git init
     ↓
git add .
     ↓
git commit
     ↓
git remote add origin
     ↓
git branch -M main
     ↓
git push
     ↓
GitHub
```

---

# 7. Clone a GitHub Repository

To copy an existing repository from GitHub:

```bash
git clone <repository-url>
```

Move into the project:

```bash
cd project-name
```

Flow:

```text
GitHub Repository
       ↓
   git clone
       ↓
Local Machine
       ↓
Project Directory
```

---

# 8. Git Push

`git push` uploads local commits to the remote repository.

```bash
git push
```

Flow:

```text
Local Repository
       ↓
    git push
       ↓
GitHub Repository
```

---

# 9. Git Pull

`git pull` retrieves the latest changes from the remote repository and integrates them into the current branch.

```bash
git pull
```

Flow:

```text
GitHub Repository
       ↓
    git pull
       ↓
Local Repository
```

---

# 10. Git Branches

Branches allow us to work on different versions or features of a project.

Example:

```text
              main
               |
        ┌──────┴──────┐
        ↓             ↓
     feature-1     feature-2
```

---

## Create a Branch

```bash
git branch feature
```

---

## List Branches

```bash
git branch
```

---

## Switch Branch

```bash
git switch feature
```

Alternative:

```bash
git checkout feature
```

---

## Create and Switch to a Branch

```bash
git switch -c feature
```

---

## Merge a Branch

First switch to the target branch:

```bash
git switch main
```

Then merge:

```bash
git merge feature
```

Flow:

```text
feature branch
      ↓
   git merge
      ↓
main branch
```

---

## Delete a Branch

```bash
git branch -d feature
```

---

# 11. Git Branch Workflow

A common development workflow:

```text
             main
              |
              ↓
        Create Branch
              |
              ↓
          feature
              |
        ┌─────┴─────┐
        ↓           ↓
      Code         Test
        ↓           ↓
      Commit       Fix
        └─────┬─────┘
              ↓
            Push
              ↓
       Pull Request
              ↓
            Review
              ↓
            Merge
              ↓
            main
```

---

# 12. GitHub Fork

A **Fork** creates a copy of another user's GitHub repository under your own GitHub account.

Basic workflow:

```text
Original Repository
        ↓
       Fork
        ↓
Your GitHub Repository
        ↓
      Clone
        ↓
   Local Machine
        ↓
      Changes
        ↓
      Commit
        ↓
       Push
        ↓
 Pull Request
        ↓
Original Repository
```

Forking is commonly used when contributing to repositories that you do not own.

---

# 13. Pull Request

A **Pull Request (PR)** is a request to merge changes from one branch or repository into another.

Typical workflow:

```text
Fork Repository
       ↓
Clone Repository
       ↓
Create Branch
       ↓
Make Changes
       ↓
Commit Changes
       ↓
Push Branch
       ↓
Create Pull Request
       ↓
Code Review
       ↓
Merge
```

---

# 14. GitHub Contribution Workflow

Example open-source contribution:

```text
Original Repository
        ↓
       Fork
        ↓
Your Repository
        ↓
      Clone
        ↓
Create Feature Branch
        ↓
Make Changes
        ↓
Commit
        ↓
Push
        ↓
Pull Request
        ↓
Maintainer Review
        ↓
Merge
```

---

# 15. Git vs GitHub

## Git

Git is a **distributed version control system** used to track changes in source code.

Git runs on the local machine and manages:

```text
Version History
Branches
Commits
Merges
Changes
```

---

## GitHub

GitHub is a platform for:

```text
Hosting Git Repositories
Collaboration
Pull Requests
Code Reviews
Issue Tracking
Open-Source Projects
```

---

## Simple Difference

```text
Git
 ↓
Version Control Tool

GitHub
 ↓
Repository Hosting & Collaboration Platform
```

Git and GitHub work together, but they are not the same thing.

---

# 16. Git Workflow – Complete View

```text
                 Git Workflow

              Working Directory
                      |
                  git add
                      ↓
                Staging Area
                      |
                git commit
                      ↓
                Local Repository
                      |
                  git push
                      ↓
               GitHub Repository
                      |
                  git pull
                      ↓
                Local Repository
```

---

# 17. Git Repository Structure

A Git repository contains the `.git` directory.

Example:

```text
gitproject/
│
├── .git/
│
├── README.md
├── index.html
├── app.java
└── pom.xml
```

The `.git` directory contains Git's repository data and history.

---

# 18. Common Git Commands

| Command                 | Purpose                               |
| ----------------------- | ------------------------------------- |
| `git --version`         | Check Git version                     |
| `git config`            | Configure Git                         |
| `git init`              | Initialize repository                 |
| `git status`            | Check repository status               |
| `git add .`             | Stage all changes                     |
| `git commit`            | Create a commit                       |
| `git log`               | View commit history                   |
| `git diff`              | View changes                          |
| `git branch`            | Manage branches                       |
| `git switch`            | Switch branches                       |
| `git merge`             | Merge branches                        |
| `git clone`             | Clone repository                      |
| `git push`              | Upload commits                        |
| `git pull`              | Retrieve and integrate remote changes |
| `git remote -v`         | View remote repository                |
| `git remote add origin` | Add remote repository                 |

---

# 19. Git Command Cheat Sheet

```bash
# Check Git version
git --version

# Configure username
git config --global user.name "Your Name"

# Configure email
git config --global user.email "your@email.com"

# View configuration
git config --list

# Initialize repository
git init

# Check status
git status

# Add a file
git add filename

# Add all files
git add .

# Commit changes
git commit -m "Initial commit"

# View history
git log

# View changes
git diff

# Add remote
git remote add origin <repository-url>

# View remote
git remote -v

# Rename branch
git branch -M main

# Push code
git push -u origin main

# Clone repository
git clone <repository-url>

# Pull latest changes
git pull

# Create branch
git branch feature

# Switch branch
git switch feature

# Create and switch branch
git switch -c feature

# Merge branch
git merge feature

# Delete branch
git branch -d feature
```

---

# 20. Git + GitHub in DevOps

Git and GitHub are important foundations for DevOps.

They support:

```text
Version Control
      ↓
Source Code Management
      ↓
Branching
      ↓
Collaboration
      ↓
Code Review
      ↓
CI/CD Integration
```

A typical DevOps workflow:

```text
Developer
    ↓
Git
    ↓
GitHub
    ↓
Jenkins / GitHub Actions
    ↓
Build
    ↓
Test
    ↓
Package
    ↓
Deploy
```

---

# 21. GitHub + Jenkins

GitHub can be integrated with Jenkins to automate CI/CD.

Example:

```text
Developer
    ↓
Git Push
    ↓
GitHub
    ↓
Webhook
    ↓
Jenkins
    ↓
Build
    ↓
Test
    ↓
Package
    ↓
Deploy
```

This allows code changes to automatically trigger CI/CD workflows.

---

# 22. Key Concepts Learned

Through my Git and GitHub practice, I learned:

```text
✓ Version Control System
✓ Git
✓ GitHub
✓ Working Directory
✓ Staging Area
✓ Local Repository
✓ Remote Repository
✓ Commit
✓ Branch
✓ Merge
✓ Clone
✓ Push
✓ Pull
✓ Fork
✓ Pull Request
✓ Git Configuration
✓ GitHub Collaboration
✓ Git + CI/CD Integration
```

---

# 23. Git Learning Journey

The overall Git workflow I learned is:

```text
Create Code
     ↓
Git Repository
     ↓
Track Changes
     ↓
Stage Changes
     ↓
Commit Changes
     ↓
Create Branches
     ↓
Merge Changes
     ↓
Push to GitHub
     ↓
CI/CD Pipeline
```

---

# 24. Final Learning

Git provides **version control**, while GitHub provides a platform for **hosting and collaboration**.

The main workflow is:

```text
Working Directory
        ↓
Staging Area
        ↓
Local Repository
        ↓
GitHub
        ↓
CI/CD
```

Git and GitHub form an important foundation for modern DevOps workflows and help developers manage source code, collaborate with teams, and connect code repositories with CI/CD automation.

---

# 25. Next Step in My DevOps Journey

After learning Git and GitHub, the next major topic in my DevOps learning journey is:

```text
Git & GitHub
      ↓
    Maven
      ↓
   Jenkins
      ↓
    CI/CD
      ↓
   AWS / Cloud
```

**Learn → Practice → Automate → Troubleshoot → Improve 🚀**
