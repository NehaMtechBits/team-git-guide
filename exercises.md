🏋️‍♀️ Practice Exercises: Let’s Build Muscle Memory
Reading is one thing, but doing is how we truly learn. These exercises will walk you through the standard workflow on a safe, shared practice repository.

Setup: The Practice Repository
Before you begin, one person on the team should create a new, public, empty repository on GitHub named team-git-practice. Do not add a README or any other files. Share the clone URL with everyone.

Exercise 1: Your First Contribution
Goal: To clone a repository, create a file, and make your first commit and push.

Clone the Repository:

Bash

git clone <paste-the-repository-url-here>
Navigate into the Folder:

Bash

cd team-git-practice
Create Your Profile File:

PowerShell

# On Windows PowerShell
New-Item your-name.md

# On Mac/Linux
touch your-name.md
Add Content: Open the new file and add a line like: Hello, my name is [Your Name]. Save it.

Stage and Commit:

Bash

git add .
git commit -m "feat: Add [Your Name]'s profile"
Push to main: For this first exercise, we will push directly to main. This is the only time you should do this.

Bash

git push origin main
Exercise 2: The Full Team Workflow (A Feature Request)
Goal: To practice the complete, safe workflow using a branch and a Pull Request.

Get The Latest Changes:

Bash

git checkout main
git pull origin main
Create a Feature Branch: Your task is to add your favorite hobby to your profile file.

Bash

git checkout -b feature/add-hobby-[your-name]
Make Your Change: Open your personal .md file and add a new line: My favorite hobby is.... Save the file.

Stage and Commit:

Bash

git add .
git commit -m "feat: Add hobby to [Your Name]'s profile"
Push Your Branch:

Bash

git push origin feature/add-hobby-[your-name]
Open a Pull Request: Go to GitHub, open a PR, and assign a teammate to review it.

Merge and Clean Up: Once approved, merge the PR and then delete the branch on GitHub.

Exercise 3: Amending a Commit
Goal: To learn how to fix the most recent commit. This is useful if you made a typo in the commit message or forgot to include a file.

Create a Branch: Create a new branch for this task.

Bash

git checkout -b feature/amend-practice-[your-name]
Make a Change & Commit: Open your profile file and add a new line: My favorite food is.... Save it.

Bash

git add .
git commit -m "feat: Add faverite food"
Notice the typo in "favorite"!

Amend the Commit Message: You haven't pushed yet, so you can easily fix it.

Bash

git commit --amend -m "feat: Add favorite food"
Forget a File: Now, create a new file called skills.md and add a skill to it.

Add the Forgotten File to the Last Commit: Stage the new file and run the amend command again.

Bash

git add skills.md
git commit --amend --no-edit
The --no-edit flag adds the new file to your previous commit without changing the commit message. Now you can push your clean, single commit.

Exercise 4: "Time Travel" to View Old Versions
Goal: To learn how to view the project's state at a previous point in time without losing any current work.

View the History: Find the commit history to locate a commit to travel to.

Bash

git log --oneline
Copy a Commit Hash: From the list, copy the short hash (the 7-character code) of an older commit.

Time Travel: Use git checkout with the hash you copied.

Bash

git checkout <paste-commit-hash-here>
You are now in a "detached HEAD" state. Look at your files—they will be exactly as they were at that point in time. You can look around, but don't make any changes.

Return to the Present:

Bash

git checkout main
Exercise 5: Cleaning Up History with Interactive Rebase
Goal: To learn how to combine multiple "work-in-progress" commits into a single, clean commit before opening a Pull Request.

Create a Branch:

Bash

git checkout -b feature/rebase-practice-[your-name]
Make Several Messy Commits: Make three separate small changes to your profile file, committing after each one.

Change 1: git add . & git commit -m "wip: start work"

Change 2: git add . & git commit -m "wip: add more stuff"

Change 3: git add . & git commit -m "wip: fix typo"

Start Interactive Rebase: Now, let's combine those three commits.

Bash

git rebase -i HEAD~3
Edit the Rebase File: Your code editor will open with a list of your last three commits. It will look like this:

pick <hash1> wip: start work
pick <hash2> wip: add more stuff
pick <hash3> wip: fix typo
Change the word pick on the second and third lines to squash (or just s).

pick <hash1> wip: start work
squash <hash2> wip: add more stuff
squash <hash3> wip: fix typo
Save and close the file.

Write the New Commit Message: Another editor window will open, allowing you to write a single, clean commit message for the combined changes. Delete the old messages and write something like: feat: Update profile with new details. Save and close.

Your three messy commits have now become one clean commit, ready for a PR.

🚨 Skill Spotlight: Resolving a Merge Conflict
Goal: To understand and fix a merge conflict. This exercise requires a partner!
(This exercise is the same as before, placed here in the flow)

Both Partners: Get the latest main branch: git checkout main and git pull origin main.

Both Partners: Create new, unique branches (e.g., conflict-A and conflict-B).

Both Partners: Open the same file and edit the exact same line to say something different.

Both Partners: Stage, commit, and push your branches.

Partner A: Open a Pull Request and merge it.

Partner B: Open a Pull Request. You will see a conflict.

Partner B (to fix):

Bring the conflict local: git checkout main, git pull, git checkout conflict-B, git merge main.

Open the file in VS Code and fix the conflict by deleting the <<<, ===, >>> markers and choosing the final code.

Finalize the merge: git add ., git commit, git push origin conflict-B. The PR can now be merged.

Exercise 7: Reverting a Bad Merge
Goal: To learn how to safely undo a change that has already been merged into main.

Create and Merge a "Mistake":

Create a new branch (feature/mistake-[your-name]).

In a file, add a line that you want to pretend is a bug (e.g., "This line breaks everything!").

Commit, push, open a PR, and merge it into main.

Find the Bad Merge Commit:

Go to the GitHub repository's main branch page.

Click on the "commits" link to see the history.

Find the merge commit for your "mistake" branch.

Revert the Pull Request:

Go to the "Pull Requests" tab and click on the "Closed" filter.

Find and click on the PR you just merged.

At the bottom, you will see a "Revert" button. Click it.

Create the Revert PR: GitHub will automatically create a new branch and a new Pull Request that contains the "opposite" of your bad changes. Simply merge this new "revert" PR.

Your "mistake" is now safely removed from the main branch, and there's a clear history showing what happened.