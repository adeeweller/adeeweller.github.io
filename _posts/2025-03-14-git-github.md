---
toc: true
author: "Adee Weller"
title: "What are Git and GitHub, and How Do I Set Them Up?"
categories:
  - Tutorial
  - Workshop
tags:
  - Git
  - GitHub
  - Version Control
  - R
header:
  image: "assets/images/git_workshop.jpg"
---

## What is Git?

Git is a free, open-source version control system that helps developers track changes to their code. It's the most widely used version control system in the world. Every coder has their own codebase and can work on it at any time. You can create branches, merge them, and delete (and undelete!) them with ease, making it very easy to track changes and revert to older versions of the code.

It is particularly popular with software developers and collaborative teams. It is not yet widely popular with political scientists (who are often hesitant about coding), but it **should be**—and is becoming more popular!

Git is open-source and free.

Git comes with a terminal called **GitBash**.

---

## What is GitHub?

GitHub is a cloud-based hosting service and website that helps software developers store, track, and collaborate on projects. It's often described as a "social network for programmers" that encourages collaboration and sharing.  

It uses Git to move files and track changes while multiple people work on the same project simultaneously.  

Developers use GitHub to showcase their code and work ethic through their profiles.  

### Getting Started with GitHub
1. Go to [GitHub](https://github.com/) and explore the interface.  
2. Click on a profile, navigate projects, and familiarize yourself with the site.  
3. Visit Adee’s **R Workshop** page—this will be our focus.  

---

## Opening Git

Think of a **repository** (*repo*) as a folder where all your code and data are stored. You can share this folder and edit it as needed.  

There are two types of repositories:  
1. A local repo (on your device).  
2. A cloud repo (on GitHub).  

### Opening GitBash (PC) or Terminal (Mac)
For Windows:  
- Type `bash` into the search bar and hit Enter.  

For Mac:  
- Open **Terminal** (or any preferred shell).  

---

## Configuring Git

Before using Git, set your user information:

```bash
git config --global user.name "Adee Weller"
git config --global user.email "adee.weller@emory.edu"
git config --global init.defaultBranch main
```

This ensures all commits are associated with your identity and sets `main` as the default branch.  

**Helpful Commands:**
- Get help for a command:  
  ```bash
  git <command> -h
  ```
- Clear the terminal:  
  ```bash
  clear
  ```

---

## Creating a Local Git Repository

### Move to Your Working Directory
```bash
cd path/to/directory
```

If the folder doesn’t exist, create one:
```bash
mkdir foldername
```

### Initialize Git Repo
```bash
git init
```

Check if it worked:
```bash
git status
```

---

## Adding Files to Git

Create a blank file:
```bash
touch newfile_AW.txt
```
*(Replace "AW" with your initials.)*  

Verify the file exists:
```bash
ls
```

Rename the file if needed:
```bash
git mv "Old_name" "New_name"
```

### Staging Files for Commit
Think of staging like preparing files before pushing them live.

Add a file to the staging area:
```bash
git add newfile_AW.txt
```

To track all files:
```bash
git add .
```

To unstage a file:
```bash
git rm --cached <filename>
```

To prevent Git from tracking specific files (e.g., sensitive data), create a `.gitignore` file.

---

## Committing Changes

A commit records a snapshot of the repository.

```bash
git commit -m "Added new file"
```

Check commit history:
```bash
git log --oneline
```

To undo a commit:
```bash
git reset ######  # Replace ###### with the commit ID
```

---

## Branching in Git

Branches allow you to work on different versions of a project.

Create a new branch:
```bash
git branch my-branch
```

List branches:
```bash
git branch
```

Switch to a branch:
```bash
git switch my-branch
```

Commit changes to the branch:
```bash
git add .
git commit -m "Changes in new branch"
```

Merge the branch back to `main`:
```bash
git merge my-branch
```

Delete the branch:
```bash
git branch -d my-branch
```

---

## Pushing Code to GitHub

### Creating a GitHub Repository
1. Go to [GitHub](https://github.com/).
2. Click "New" and create a repository.

### Linking Local Repo to GitHub
```bash
git remote add origin <repository-URL>
git branch -M main
git push -u origin main
```

To push all branches:
```bash
git push --all
```

To pull new changes:
```bash
git pull
```

---

## Cloning an Existing Repo

To work on a project from GitHub, clone it:

```bash
git clone https://github.com/adeeweller/R_Workshop.git
```

Navigate into the cloned repo:
```bash
cd R_Workshop
```

Check which remote is set:
```bash
git remote -v
```

Update remote URL if needed:
```bash
git remote set-url origin <new-link>
```

Pull with rebase to apply local changes:
```bash
git pull --rebase origin main
```

---

## Final Notes

Git and GitHub are essential tools for version control and collaboration. While political scientists are still catching on, these tools are becoming more popular in the field.

By mastering Git, you gain:

✅ Better organization.  
✅ Version control safety.  
✅ Seamless collaboration.  

Happy coding! 🚀  