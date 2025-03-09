# Git Commands

## ✔️ Check Git Version
```sh
git --version  # Check if Git is installed and display its version
```

## ✔️ Configuration - Identify Yourself
```sh
git config --global user.name "yourname"  # Set your name

git config --global user.email "youremail"  # Set your email

git config --global core.editor "code --wait"  # Set VS Code as the default editor

git config --global -e  # Open global Git settings in the editor

git config --global core.autocrlf true  # Set to 'true' for Windows, 'input' for macOS/Linux
```

## ✔️ Rename Git Command Prompts
```sh
git config --local alias.your-config-name "the main config name"# Renames git command prompts to your desired name in this project
# example below:
git config --local alias.lgo "log --oneline" # now we can simply use `lgo` to call "log --oneline"
# to use it globaly, use --global instead of --local
```

## ✔️ Initializing a Repository
```sh
git init  # Initialize a Git repository in the current directory
```

## ✔️ Workflow
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

git log --oneline # Show commit history; summarizes each commit in oneline

git log --stat # More detailed statistics show total commits.

git log --graph # Graphically displays commit history + branches

git log --graph --oneline # Graphically displays commit history + branches; summarizes each commit in oneline

git log --after="23-10-12" # displays commit history after the date "23-10-12"

git log --before="23-10-12" # displays commit history before the date "23-10-12"

git log --author="Parsa Hosseii" # displays only Parsa Hosseii commit history

git show commit-hash  # Show details of a specific commit

git show HEAD~2  # Show changes made in the commit before last two commits

git show HEAD~2:filePath  # Show changes in a specific file from two commits before

git restore --staged fileName  # Unstage a file

git checkout commit-hash  # Move to a specific commit

git checkout master  # Switch back to the latest commit in the master branch
```

## ✔️ Branches
```sh
git branch  # List all branches

git branch branchName  # Create a new branch

git checkout branchName  # Switch to another branch

git switch branchName # switch to branchName

git switch -c branchName # first creates branchName and then switch to it

git merge branchName  # Merge changes from another branch into the current branch

git branch -d branchName  # Delete a branch (only if merged with the remote branch)

git branch -D branchName  # Force delete a branch (even if not merged)

git branch -m newBranchName # Renames branch currently you are on
```
# General tips

## ✔️ Show Hidden `.git` Directory in Repository on vscode
1. Press `Ctrl + Shift + P` in VS Code.
2. Type `>settings` and select **Preferences: Open User Settings (JSON)**.
3. Change the value of `"**/.git"` from `true` to `false`.

This will make the `.git` folder visible in the file explorer.

---
---

## ✔️ Install and Use GitLens Extension in VS Code

### 1. Install GitLens Extension
1. Open **VS Code**.
2. Press `Ctrl + Shift + X` to open the Extensions Marketplace.
3. In the search bar, type **GitLens**.
4. Click on **GitLens — Git supercharged** by **GitKraken**.
5. Click **Install**.

---

### 2. Enable GitLens Features
Once installed, GitLens adds various features to your VS Code. Some of the most useful ones include:

- **File Blame:** Shows who last edited each line in a file.
- **Line History:** Displays commit history for the selected line.
- **Repository View:** Provides an overview of branches, commits, and remotes.

To enable or customize features:
1. Press `Ctrl + Shift + P` to open the Command Palette.
2. Type `GitLens: Settings` and select it.
3. Adjust the settings based on your preference.

---

### 3. Using GitLens in VS Code
#### a) View Line Blame
1. Open a **Git-tracked** file.
2. Hover over any line to see the **last commit and author** in a tooltip.

#### b) View File History
1. Right-click on a file in the Explorer panel.
2. Select **GitLens: Show File History**.

#### c) View Commit Details
1. Open the **Source Control** sidebar (`Ctrl + Shift + G`).
2. Click on a commit to see details such as **author, message, and changes**.

---

### 4. Customize GitLens in `settings.json`
1. Press `Ctrl + Shift + P`.
2. Type `>settings` and select **Preferences: Open User Settings (JSON)**.
3. Add or modify the following settings:

```json
{
  "gitlens.currentLine.enabled": true,
  "gitlens.hovers.enabled": true,
  "gitlens.codeLens.enabled": true,
  "gitlens.views.repositories.enabled": true
}

