Of course. Here is the complete, corrected content formatted as a raw Markdown code block.

Markdown

# ✅ Our Standard Team Workflow

This is the **only workflow** we will use for all projects. It is designed to be safe, prevent conflicts, and allow for code reviews.

### The Golden Rule: Never Push Directly to the `main` Branch

All new work, whether it's a feature or a bug fix, must be done on a separate branch and merged into `main` only after a review.

---

### Step-by-Step Process

Here is the exact process for adding a new feature or fixing a bug.

#### Step 1: Get the Latest Code

Before starting any new work, make sure your local `main` branch is up-to-date with the latest code from GitHub.

```bash
git checkout main
git pull origin main
```

#### Step 2: Create a New Branch

Create a new branch for the task you are working on. Naming your branch descriptively is important!

Branch Naming Conventions:

For new features: feature/short-description (e.g., feature/add-login-button)

For bug fixes: bugfix/ticket-number-or-description (e.g., bugfix/fix-header-on-mobile)

Use this single command to create the branch and switch to it immediately:

```bash

git checkout -b <your-new-branch-name>
Step 3: Do Your Work (Code & Commit Often)
Make your code changes. It is a best practice to save your work in small, logical chunks called commits.
```

```bash

# 1. Check which files you have changed
git status

# 2. Add your changed files to be "staged" for the next commit
git add .  # The '.' adds all changed files in the current folder

# 3. Save your work with a clear message
git commit -m "feat: Add user email field to login form"
```

```bash

Step 4: Push Your Branch to GitHub
When you are ready to share your work or open it for review, push your new branch and its commits to the remote repository on GitHub.
```

```bash

git push origin <your-new-branch-name>
```

#### Step 5: Open a Pull Request (PR)

A Pull Request is a formal request to merge your changes into the main branch.

Go to the repository on GitHub.

You will see a green button to "Compare & pull request" for your recently pushed branch. Click it.

Give your PR a clear title and a brief description of what you did.

On the right side, assign at least one team member to review your code.

Click "Create pull request."

#### Step 6: Review, Merge, and Clean Up

Your reviewer will look at the code, may ask for changes, and will eventually approve it.

Once approved, the person who opened the PR (you!) is responsible for merging it by clicking the "Merge pull request" button on GitHub.

Delete your branch after merging. GitHub provides a button for this right after you merge. This keeps our repository clean.

Finally, go back to your local machine and update your main branch again.

```bash

git checkout main
git pull origin main

```
