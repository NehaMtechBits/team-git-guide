# 🏋️‍♀️ Practice Exercises: Let's Build Muscle Memory

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
    Go to the GitHub repository online to see your file! Wait for your teammates to do the same.

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

### 🚨 Skill Spotlight: Resolving a Merge Conflict

**This is one of the most important skills you will learn.** Conflicts happen when two people change the same line of the same file. They are not errors; they are simply Git asking you, a human, to make a decision about which code to keep.

**Goal:** To understand and fix a merge conflict. **This exercise requires a partner!**

1.  **Both Partners:** Get the latest `main` branch.
    ```bash
    git checkout main
    git pull origin main
    ```
2.  **Both Partners:** Create a new branch with a unique name (e.g., `conflict-A` and `conflict-B`).

3.  **Both Partners:** Open the **same file** and edit the **exact same line** to say something different. For example:

    - Partner A changes line 1 to: `Project Status: Alpha`
    - Partner B changes line 1 to: `Project Status: Beta`

4.  **Both Partners:** Stage, commit, and push your respective branches.

5.  **Partner A:** Open a Pull Request and merge it. This will succeed.

6.  **Partner B:** Open a Pull Request. GitHub will now show the message: **"This branch has conflicts that must be resolved."**

7.  **Partner B (to fix the conflict):**
    _ **Bring the conflict to your local machine:**
    `bash
        git checkout main
        git pull origin main  # Get Partner A's change
        git checkout conflict-B # Go back to your branch
        git merge main        # This triggers the conflict locally
        `
    _ **Open the file in VS Code.** You'll see conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`). VS Code also provides helpful buttons like "Accept Current Change" or "Accept Incoming Change".
    _ **Resolve the conflict.** Manually edit the file to be correct. Delete all the `<<<`, `===`, and `>>>` markers. For example, decide to keep the line as `Project Status: Beta`.
    _ **Finalize the merge:**
    `bash
        git add .
        git commit  # No message needed, a default one will be provided
        git push origin conflict-B
        `
    The Pull Request on GitHub will now be conflict-free and can be merged!
