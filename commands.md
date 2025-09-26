# 📚 Essential Git Commands Cheat Sheet

You don't need to memorize every Git command. For our daily workflow, you will only need these few.

# 📚 Essential Git Commands Cheat Sheet

You don't need to memorize every Git command. For our daily workflow, you will only need these few.

---

### Local Workflow: Getting Set Up & Making Changes

| Command                          | Description                                                                                                            |
| :------------------------------- | :--------------------------------------------------------------------------------------------------------------------- |
| `git clone <url>`                | **Get the code:** Downloads a copy of a remote repository to your computer. You only do this once per project.         |
| `git pull origin main`           | **Get updates:** Downloads the latest changes from the `main` branch on GitHub to your local machine.                  |
| `git status`                     | **Check your work:** Shows you which files have been changed, which are new, and which are staged for the next commit. |
| `git add .`                      | **Stage your changes:** Adds all your modified and new files to the "staging area," getting them ready for a commit.   |
| `git commit -m "message"`        | **Save your work:** Creates a permanent snapshot (a commit) of your staged changes with a descriptive message.         |
| `git log` or `git log --oneline` | **See history:** Shows the history of commits on your current branch. The `--oneline` flag makes it more compact.      |

### Collaboration: Working with Branches & GitHub

| Command                         | Description                                                                                                        |
| :------------------------------ | :----------------------------------------------------------------------------------------------------------------- |
| `git checkout -b <branch-name>` | **Create a new branch:** Creates a new branch and immediately switches to it. This is how you start any new task.  |
| `git push origin <branch-name>` | **Share your work:** Uploads all your local commits from your current branch to GitHub.                            |
| `git checkout <branch-name>`    | **Switch branches:** Changes your current working directory to a different branch.                                 |
| `git branch`                    | **List branches:** Shows you all the branches on your local machine and highlights which one you are currently on. |

## How to Create and Push the File

Create the file in your project folder:

```bash
New-Item commands.md
```

Copy and paste the content above into the new commands.md file and save it.

Add, commit, and push the new file to your GitHub repository:

```bash

git add commands.md
git commit -m "docs: Add commands cheat sheet"
git push origin main

```
