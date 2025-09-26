# 📚 Essential Git Commands Cheat Sheet

You don't need to memorize every Git command. For our daily workflow, you will only need these few.

---

### ## Getting Started & Daily Updates

This is how you start with a project and get the latest changes each day.

| Command                | Description                                                                                                                        |
| :--------------------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| `git clone <url>`      | **Get the code:** Downloads a copy of a remote repository. (You only do this once per project).                                    |
| `git pull origin main` | **Get updates:** Downloads and merges the latest changes from GitHub into your current branch. (Do this before starting new work). |

---

### ## The Core Workflow: Creating a Feature

This is the step-by-step cycle for every new task.

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

These commands help you see where you are and what has happened.

| Command                      | Description                                                        |
| :--------------------------- | :----------------------------------------------------------------- |
| `git log --oneline`          | **See history:** Shows a compact history of all the commits.       |
| `git branch`                 | **List branches:** Shows all branches on your local machine.       |
| `git checkout <branch-name>` | **Switch branches:** Changes your view to another existing branch. |

---

### ## Deeper Concept: `git fetch` vs. `git pull`

This is an important difference to understand as you get more comfortable with Git.

| Command                | Description                                                                                                                                                             |
| :--------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `git fetch origin`     | **Downloads without merging:** Fetches all new changes from the remote but doesn't apply them. This is a safe way to review updates before merging them into your work. |
| `git pull origin main` | **Downloads AND merges:** A shortcut that runs `git fetch` and `git merge` in one step. It's more direct but less controlled.                                           |
