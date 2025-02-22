# Git Commands

## Check Git Version
```sh
git --version  # Check if Git is installed and display its version
```

## Configuration - Identify Yourself
```sh
git config --global user.name "yourname"  # Set your name

git config --global user.email "youremail"  # Set your email

git config --global core.editor "code --wait"  # Set VS Code as the default editor

git config --global -e  # Open global Git settings in the editor

git config --global core.autocrlf true  # Set to 'true' for Windows, 'input' for macOS/Linux
```

## Initializing a Repository
```sh
git init  # Initialize a Git repository in the current directory
```

## Workflow
```sh
git status  # Show untracked, staged, and modified files

git add fileName  # Add a file to the staging area

git commit -m "your message here"  # Commit changes with a message

git commit -a -m "your message here"  # Commit all tracked files without staging

git rm filename  # Remove a file from directory and staging area

git mv oldFilename newFilename  # Rename a file

git diff  # Show changes in files

git diff --staged  # Show changes in staged files

git log  # Show commit history

git show commit-hash  # Show details of a specific commit

git show HEAD~2  # Show changes made in the commit before last two commits

git show HEAD~2:filePath  # Show changes in a specific file from two commits before

git restore --staged fileName  # Unstage a file

git checkout commit-hash  # Move to a specific commit

git checkout master  # Switch back to the latest commit in the master branch
```

## Branches
```sh
git branch  # List all branches

git branch branchName  # Create a new branch

git checkout branchName  # Switch to another branch

git merge branchName  # Merge changes from another branch into the current branch

git branch -d branchName  # Delete a branch (only if merged with the remote branch)

git branch -D branchName  # Force delete a branch (even if not merged)
```
# General tips

## Show Hidden `.git` Directory in Repository on vscode
1. Press `Ctrl + P` in VS Code.
2. Type `>settings` and select **Preferences: Open User Settings (JSON)**.
3. Change the value of `"**/.git"` from `true` to `false`.

This will make the `.git` folder visible in the file explorer.
