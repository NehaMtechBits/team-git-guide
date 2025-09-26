# 🏋️‍♀️ Practice Exercises: Let’s Build Muscle Memory

Reading is one thing, but doing is how we truly learn. These exercises will walk you through the standard workflow on a safe, shared practice repository.

### Setup: The Practice Repository

Before you begin, one person on the team should create a new, **public, empty repository** on GitHub named `team-git-practice`. Do not add a README or any other files. Share the clone URL with everyone.

---

### Exercise 1: Your First Contribution

**Goal:** To clone a repository, create a file, and make your first commit and push.

1.  **Clone the Repository:**
    ```bash
    git clone <paste-the-repository-url-here>
    ```
2.  **Navigate into the Folder:**
    ```bash
    cd team-git-practice
    ```
3.  **Create Your Profile File:**
    ```powershell
    # On Windows PowerShell
    New-Item your-name.md

    # On Mac/Linux
    touch your-name.md
    ```
4.  **Add Content:** Open the new file and add a line like: `Hello, my name is [Your Name]`. Save it.

5.  **Stage and Commit:**
    ```bash
    git add .
    git commit -m "feat: Add [Your Name]'s profile"
    ```
6.  **Push to `main`:** For this first exercise, we will push directly to `main`. **This is the only time you should do this.**
    ```bash
    git push origin main
    ```

---

### Exercise 2: The Full Team Workflow (A Feature Request)

**Goal:** To practice the complete, safe workflow using a branch and a Pull Request.

1.  **Get The Latest Changes:**
    ```bash
    git checkout main
    git pull origin main
    ```
2.  **Create a Feature Branch:** Your task is to add your favorite hobby to your profile file.
    ```bash
    git checkout -b feature/add-hobby-[your-name]
    ```
3.  **Make Your Change:** Open your personal `.md` file and add a new line: `My favorite hobby is...`. Save the file.

4.  **Stage and Commit:**
    ```bash
    git add .
    git commit -m "feat: Add hobby to [Your Name]'s profile"
    ```
5.  **Push Your Branch:**
    ```bash
    git push origin feature/add-hobby-[your-name]
    ```
6.  **Open a Pull Request:** Go to GitHub, open a PR, and assign a teammate to review it.

7.  **Merge and Clean Up:** Once approved, merge the PR and then delete the branch on GitHub.

---

### Exercise 3: Amending a Commit

**Goal:** To learn how to fix the most recent commit. This is useful if you made a typo in the commit message or forgot to include a file.

1.  **Create a Branch:**
    ```bash
    git checkout -b feature/amend-practice-[your-name]
    ```
2.  **Make a Change & Commit:** Open your profile file and add a new line: `My favorite food is...`. Save it.
    ```bash
    git add .
    git commit -m "feat: Add faverite food"
    ```
    Notice the typo in "favorite"!

3.  **Amend the Commit Message:**
    ```bash
    git commit --amend -m "feat: Add favorite food"
    ```
4.  **Forget a File:** Now, create a new file called `skills.md` and add a skill to it.
5.  **Add the Forgotten File to the Last Commit:**
    ```bash
    git add skills.md
    git commit --amend --no-edit
    ```
    The `--no-edit` flag adds the new file to your previous commit without changing the message.

---

### Exercise 4: "Time Travel" to View Old Versions

**Goal:** To learn how to view the project's state at a previous point in time.

1.  **View the History:**
    ```bash
    git log --oneline
    ```
2.  **Copy a Commit Hash:** From the list, copy the short hash (the 7-character code) of an older commit.
3.  **Time Travel:**
    ```bash
    git checkout <paste-commit-hash-here>
    ```
    You are now in a "detached HEAD" state. Look at your files to see how they existed in the past.
4.  **Return to the Present:**
    ```bash
    git checkout main
    ```

---

### Exercise 5: Cleaning Up History with Interactive Rebase

**Goal:** To learn how to combine multiple "work-in-progress" commits into a single, clean commit before opening a Pull Request.

1.  **Create a Branch:**
    ```bash
    git checkout -b feature/rebase-practice-[your-name]
    ```
2.  **Make Several Messy Commits:** Make three separate small changes, committing after each one with messages like "wip: start work", "wip: add more stuff", and "wip: fix typo".
3.  **Start Interactive Rebase:**
    ```bash
    git rebase -i HEAD~3
    ```
4.  **Edit the Rebase File:** Your editor will open. Change the word `pick` on the second and third lines to `squash` (or `s`). Save and close.
5.  **Write the New Commit Message:** Another editor window will open. Delete the old messages and write a single, clean message like: `feat: Update profile with new details`. Save and close. Your three commits are now one.

---

### Exercise 6: Resolving a Merge Conflict (Skill Spotlight 🚨)

**Goal:** To understand and fix a merge conflict. **This exercise requires a partner!**

1.  **Both Partners:** Get the latest `main` branch: `git checkout main` and `git pull origin main`.
2.  **Both Partners:** Create new, unique branches (e.g., `conflict-A` and `conflict-B`).
3.  **Both Partners:** Open the **same file** and edit the **exact same line** to say something different.
4.  **Both Partners:** Stage, commit, and push your branches.
5.  **Partner A:** Open a Pull Request and merge it.
6.  **Partner B:** Open a Pull Request. You will see a conflict.
7.  **Partner B (to fix):**
    * Bring the conflict local:
        ```bash
        git checkout main
        git pull
        git checkout conflict-B
        git merge main
        ```
    * Open the file in VS Code and fix the conflict by deleting the `<<<`, `===`, `>>>` markers and choosing the final code.
    * Finalize the merge:
        ```bash
        git add .
        git commit
        git push origin conflict-B
        ```
    The PR can now be merged.

---

### Exercise 7: Reverting a Bad Merge

**Goal:** To learn how to safely undo a change that has already been merged into `main`.

1.  **Create and Merge a "Mistake":** Create a new branch, add a line that you want to pretend is a bug, and merge it into `main` via a Pull Request.
2.  **Find the Bad Merge Commit:** On GitHub, go to the "Pull Requests" tab and click on the "Closed" filter. Find and click on the PR you just merged.
3.  **Revert the Pull Request:** At the bottom, click the **"Revert"** button.
4.  **Create the Revert PR:** GitHub will automatically create a new branch and a Pull Request. Simply merge this new "revert" PR. Your "mistake" is now safely undone.