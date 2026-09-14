# Git-GitHub-Cheat-Sheet
A quick reference guide for the Git and GitHub concepts and commands I learned during my DevOps learning journey.

1. Git Workflow
Working Directory
       ↓
Staging Area
       ↓
Local Repository
       ↓
Remote Repository (GitHub)
Working Directory

The location where we create and modify our files.

Staging Area

The area where we prepare changes before committing.

Local Repository

The Git repository stored on our local machine.

Remote Repository

A repository hosted on a remote platform such as GitHub.

2. Git Configuration
git --version
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list
3. Create a Repository
mkdir gitproject
cd gitproject
git init

Check repository status:

git status
4. Basic Git Commands
Add files
git add filename
git add .
Commit changes
git commit -m "Initial commit"
View commit history
git log
View changes
git diff
5. Connect Git to GitHub
git remote add origin <repository-url>
git remote -v

Rename the branch to main:

git branch -M main

Push code to GitHub:

git push -u origin main
6. Clone a GitHub Repository
git clone <repository-url>

Move into the project:

cd project-name
7. Pull and Push
Push

Upload local changes to GitHub:

git push
Pull

Download the latest changes from GitHub:

git pull
8. Branches

Create a branch:

git branch feature

List branches:

git branch

Switch branches:

git switch feature

Or:

git checkout feature

Create and switch to a branch:

git switch -c feature

Merge a branch:

git merge feature

Delete a branch:

git branch -d feature
9. GitHub Fork

A fork creates a copy of another user's GitHub repository under your own GitHub account.

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
Commit + Push
        ↓
Pull Request
        ↓
Original Repository

Forking is commonly used when contributing to projects that you don't own.

10. Pull Request

A Pull Request (PR) is a request to merge changes from one branch/repository into another.

Typical workflow:

Fork Repository
       ↓
Clone Repository
       ↓
Create Branch
       ↓
Make Changes
       ↓
Commit
       ↓
Push
       ↓
Create Pull Request
       ↓
Review
       ↓
Merge
11. Useful Git Commands
Command	Purpose
git init	Initialize repository
git status	Check status
git add .	Stage all changes
git commit -m "message"	Save changes
git log	View history
git diff	View differences
git branch	List branches
git switch	Switch branches
git merge	Merge branches
git clone	Copy remote repository
git push	Upload changes
git pull	Download latest changes
git remote -v	View remote repository
git remote add origin	Add remote repository
12. Git vs GitHub
Git

Git is a distributed version control system used to track changes in source code.

GitHub

GitHub is a cloud-based platform used to host Git repositories and collaborate with developers.

Git = Version Control Tool
GitHub = Platform for Hosting & Collaboration
13. Key Concepts I Learned
Version Control System (VCS)
Git
GitHub
Working Directory
Staging Area
Local Repository
Remote Repository
Commit
Branch
Merge
Clone
Push
Pull
Fork
Pull Request
14. My DevOps Learning Journey

Git and GitHub are important foundations for DevOps because they support:

Version control
Team collaboration
Code management
Branching strategies
CI/CD workflows
Open-source contribution

I am continuing my DevOps learning journey and moving toward learning Maven as my next major topic.
