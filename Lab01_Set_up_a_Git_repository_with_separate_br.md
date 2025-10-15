# Lab 01: Set up a Git repository with separate branches for frontend and backend, then merge them into the main branch.

## Objective
The objective of this lab is to demonstrate how to initialize a Git repository, create and manage branches for different parts of a project (frontend and backend), and finally merge them into the main branch.
This exercise helps in understanding Git branching, merging, and collaboration workflow, which are essential in real-world software development.

## Tools / Technologies
Git – for version control and branching
GitHub – for hosting the remote repository
Command Line Interface (CLI) – to execute Git commands
(Optional) VS Code or any IDE – to view/edit project files

## Prerequisites
Git is installed and configured (git --version)
GitHub account is created and accessible
Basic knowledge of command-line operations
Internet connection for pushing changes to GitHub
## Steps / Commands
1. Initialize a New Git Repository
mkdir Lab01_GitDemo
cd Lab01_GitDemo
git init
2. Create a README File
echo "# Lab01 Git Demo Project" > README.md
git add README.md
git commit -m "Initial commit with README"
3. Create and Switch to the Frontend Branch
git branch frontend
git checkout frontend
4. Add Frontend Code
echo "<h1>Frontend Home Page</h1>" > index.html
git add index.html
git commit -m "Added frontend index.html"
5. Create and Switch to the Backend Branch
git checkout main
git branch backend
git checkout backend
6. Add Backend Code
echo "print('Backend Server Running')" > server.py
git add server.py
git commit -m "Added backend server.py"
7. Merge Frontend and Backend into Main
git checkout main
git merge frontend
git merge backend
8. Connect to Remote Repository (GitHub)
git remote add origin https://github.com/<your-username>/Lab01_GitDemo.git
git branch -M main
git push -u origin main
9. Push All Branches
git push origin frontend
git push origin backend
## Expected Output / Result
Three branches on GitHub: main, frontend, and backend
Main branch contains merged code from both frontend and backend
Successful output messages from each Git command
Screenshot example:
git branch output showing all branches
git log --oneline --graph showing merge historyThree branches on GitHub: main, frontend, and backend
Main branch contains merged code from both frontend and backend
Successful output messages from each Git command
Screenshot example:
git branch output showing all branches
git log --oneline --graph showing merge history
## DeLabs/Lab01_GitDemo.md — Completed report file
Lab1_files/ — Folder containing:
Screenshots of git branch, git log, and successful merges
Source files (index.html, server.py, README.md)liverables (what to push)
## Notes / Tips
Always commit before switching branches to avoid data loss.
Use git status frequently to track changes.
If a merge conflict occurs:
git status
# Edit conflicting files manually
git add <file>
git commit
You can visualize branches using:
git log --oneline --graph --all
