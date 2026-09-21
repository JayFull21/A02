# A02: A Beginner Git, GitHub, and WebStorm guide

## Introduction

This tutorial is written so that anyone — even someone who has never used version control before — can follow along and learn how to create a GitHub account, set up a repository, and use Git commands to track and share code. 
---

## How to Use Git and GitHub

### Step 1: Create a GitHub Account

1. Go to [https://github.com/join](https://github.com/join).
2. Enter a username, email address, and password.
3. Verify your email address by clicking the confirmation link GitHub sends you.
4. Choose the free plan when prompted (this is sufficient for coursework and personal projects).

### Step 2: Install Git 

Before you can use Git commands, Git itself must be installed locally.

1. Go to [https://git-scm.com/downloads](https://git-scm.com/downloads).
2. Download the installer for your operating system (Windows, macOS, or Linux).
3. Run the installer and accept the default settings unless you have a specific reason to change them.
4. Confirm the installation by opening a terminal (Command Prompt, PowerShell, or Terminal) and typing:
   ```
   git --version
   ```
   If Git is installed correctly, this will print a version number.

### Step 3: Configure Git 

Git attaches a name and email to every **commit** you make, so this only needs to be done once per machine:

```
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

### Step 4: Create a New Repository 

1. Log into GitHub and click the **+** icon 
2. Name the repository exactly as you want 
3. Choose **Public** or **Private** depending on the assignment requirements.
4. Check the box to **Add a README file** so the repository is initialized with a `README.md` file you can edit.
5. Click **Create repository**.


### Step 5: Clone the Repo to Your Computer


1. On your repository's GitHub page, click the green **Code** button and copy the HTTPS URL.
2. In your terminal, go to the folder where you want the project to live, then run:
   ```
   git clone https://github.com/yourUsername/filename.git
   ```
3. Move into the new folder:
   ```
   cd filename
   ```

### Step 6: Make Changes and Track Them

1. Open the project folder in your code editor.
2. Check which files have changed:
   ```
   git status
   ```
3. Stage the files you want to include in your next commit:
   ```
   git add file
   ```
   (Use `git add .` to stage every changed file at once.)

### Step 7: Commit Your Changes


```
git commit -m "Task: Create Repository"
git commit -m "Feature: added workflow for using github"
git commit -m "Fix: changed readme.md for definition of terms"
```

- **Task:** — setup or administrative work (creating files, folders, repositories)
- **Feature:** — new functionality or content added
- **Fix:** — corrections to existing content or code

### Step 8: Push Your Changes to GitHub

```
git push origin main
```

### Step 9: Pull Changes From GitHub


```
git pull origin main
```

### Step 10: Working With Branches 

A **branch** lets you work on a new feature or fix without affecting the main version of the project.

1. Create and switch to a new branch:
   ```
   git checkout -b new-feature
   ```
2. Make your changes, then `add` and `commit` as usual.
3. Push the branch to GitHub:
   ```
   git push origin new-feature
   ```

---

## PART 1: Directions on Using WebStorm

WebStorm is a JetBrains code editor with built-in Git and GitHub integration, which means you can clone, commit, push, and pull without leaving the editor.

1. **Download WebStorm.** Go to [https://www.jetbrains.com/webstorm/download](https://www.jetbrains.com/webstorm/download) and download the installer for your operating system. WebStorm is free for students through the [JetBrains Student Pack](https://www.jetbrains.com/community/education/#students).
2. **Install WebStorm.** Run the downloaded installer and follow the setup wizard, accepting the default installation options.
3. **Launch WebStorm and sign in.** On first launch, you can optionally log in with a JetBrains account to activate a student or trial license.
4. **Clone your repository directly in WebStorm:**
   - On the Welcome screen, select **Get from VCS**.
   - Paste your repository URL (`https://github.com/yourUsername/A02.git`).
   - Choose a local folder and click **Clone**.
5. **Connect your GitHub account (if not already prompted):** Go to **Settings/Preferences → Version Control → GitHub**, click the **+**, and log in to authorize WebStorm to access your GitHub account.
6. **Edit your files.** Open `README.md` from the project panel on the left and make your edits directly in the editor.
7. **Stage and commit changes in WebStorm:**
   - Go to **Git → Commit** (or press `Ctrl+K` / `Cmd+K`).
   - Check the box next to the files you want to include.
   - Type a commit message (e.g., `Feature: added workflow for using github`) and click **Commit**.
8. **Push changes to GitHub:**
   - Go to **Git → Push** (or press `Ctrl+Shift+K` / `Cmd+Shift+K`).
   - Review the commits being pushed, then click **Push**.
9. **Pull changes from GitHub:** Go to **Git → Pull** to fetch and merge any updates from the remote repository into your local project.

---

## PART 2: Glossary

- **Branch** – A separate line of development within a repository that allows changes to be made without affecting the main codebase until they are ready to be merged.
- **Clone** – The act of creating a full local copy of a remote repository, including its entire history.
- **Commit** – A saved snapshot of staged changes in a repository, recorded with a message describing what was changed.
- **Fetch** – The act of downloading new data (commits, branches, tags) from a remote repository without merging it into your local branches.
- **GIT** – A distributed version control system used to track changes to files over time and coordinate work among multiple people.
- **Github** – A web-based hosting platform for Git repositories that adds collaboration features such as pull requests, issues, and project boards.
- **Merge** – The process of combining changes from one branch into another.
- **Merge Conflict** – A situation that occurs when Git cannot automatically reconcile differing changes to the same part of a file, requiring manual resolution.
- **Push** – The act of uploading local commits to a remote repository so they become available to others.
- **Pull** – The act of fetching changes from a remote repository and merging them into the current local branch in a single step.
- **Remote** – A version of a repository that is hosted on a server (such as GitHub) rather than on your local machine.
- **Repository** – A storage location for a project's files and their complete version history.

---

## References

Git. (n.d.). *Git downloads*. Software Freedom Conservancy. https://git-scm.com/downloads

GitHub, Inc. (n.d.). *Sign up for GitHub*. https://github.com/join

GitHub Docs. (n.d.). *Get started with Git and GitHub*. https://docs.github.com/en/get-started

JetBrains. (n.d.). *Download WebStorm*. https://www.jetbrains.com/webstorm/download

JetBrains. (n.d.). *WebStorm documentation: Install and set up WebStorm*. https://www.jetbrains.com/help/webstorm/installation-guide.html