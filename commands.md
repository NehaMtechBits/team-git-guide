# 📚 Essential Git Commands Cheat Sheet

You don't need to memorize every Git command. For our daily workflow, you will only need these few.

---

### ## Starting a Project

| Command           | Description                                                                                                                                         |
| :---------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| `git clone <url>` | **For existing projects:** Downloads and prepares a copy of a remote repository. This is the most common way to start.                              |
| `git init`        | **For brand-new projects:** Creates a new, empty Git repository in your current folder. Use this only when starting a project locally from scratch. |

---

### ## Daily Updates

| Command                | Description                                                                                             |
| :--------------------- | :------------------------------------------------------------------------------------------------------ |
| `git pull origin main` | **Get updates:** Downloads and merges the latest changes from GitHub. Do this before starting new work. |

---

### ## The Core Workflow: Creating a Feature

| Command                         | Description                                                                                      |
| :------------------------------ | :----------------------------------------------------------------------------------------------- |
| `git checkout -b <branch-name>` | **1. Create a branch:** Creates a new branch for your task and switches to it.                   |
| `git status`                    | **2. Check your work:** Shows which files you have changed.                                      |
| `git diff`                      | **3. See change details:** Shows the exact line-by-line changes in your files.                   |
| `git add .`                     | **4. Stage your changes:** Prepares your changed files to be saved.                              |
| `git commit -m "message"`       | **5. Save your changes:** Creates a commit (a save point) of your staged files.                  |
| `git push origin <branch-name>` | **6. Share your work:** Uploads your branch and its commits to GitHub, ready for a Pull Request. |

---

### ## Useful Commands for Navigation

| Command                      | Description                                                        |
| :--------------------------- | :----------------------------------------------------------------- |
| `git log --oneline`          | **See history:** Shows a compact history of all the commits.       |
| `git branch`                 | **List branches:** Shows all branches on your local machine.       |
| `git checkout <branch-name>` | **Switch branches:** Changes your view to another existing branch. |

---

### ## Deeper Concept: `git fetch` vs. `git pull`

| Command                | Description                                                                                                                     |
| :--------------------- | :------------------------------------------------------------------------------------------------------------------------------ |
| `git fetch origin`     | **Downloads without merging:** Fetches new changes but doesn't apply them. This is a safe way to review updates before merging. |
| `git pull origin main` | **Downloads AND merges:** A shortcut that runs `git fetch` and `git merge` in one step.                                         |
