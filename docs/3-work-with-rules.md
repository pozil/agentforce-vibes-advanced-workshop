# Exercise 3: Work with Rules

<p align="center">
   <a href="2-vibe-code-a-component.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="4-work-with-workflows.md">Next Exercise ▶︎</a>
</p>

---

In this exercise, you'll configure git and work with [Rules](https://developer.salesforce.com/docs/platform/einstein-for-devs/guide/devagent-rules.html).


## Step 1: Configure git

1. Run this command in the terminal where `YOUR_GITHUB_EMAIL` is your GitHub account email:

   ```shell
   git config --global user.email "YOUR_GITHUB_EMAIL"
   ```

2. Run this command in the terminal where `YOUR_GITHUB_USERNAME` is your GitHub username:

   ```shell
   git config --global user.name "YOUR_GITHUB_USERNAME"
   ```


## Step 2: Prepare the local git repository

1. Run this batch of commands in the terminal to remove unneeded files from the project:

   ```shell
   rm -fr scripts
   rm -fr force-app/main/default/applications
   rm -fr force-app/main/default/aura
   rm -fr force-app/main/default/contentassets
   rm -fr force-app/main/default/flexipages
   rm -fr force-app/main/default/layouts
   rm -fr force-app/main/default/permissionsets
   rm -fr force-app/main/default/staticresources
   rm -fr force-app/main/default/tabs
   rm -fr force-app/main/default/triggers
   rm *.vsix
   ```

2. Run these commands in the terminal to initialize a local git repository and create an initial commit:

   ```shell
   git init
   git add --all -- ':!force-app/main/default/classes' ':!force-app/main/default/lwc'
   git commit -m "feat: initial commit"
   ```

> [!NOTE]
> We've excluded Apex and LWC from the initial commit. We'll add them in a separate commit.


## Step 3: Create a rule for git conventions

1. From the **Agentforce Vibes Sidebar**, click the **Manage Agentforce Rules & Workflows** (balance) icon:

   ![Icon for Manage Agentforce Rules & Workflows](../assets/3-rules-icon.png)

2. Make sure that you're on the **Rules** tab.

3. Enter `custom-git-conventions.md` under the **Workspace Rules** section.

4. Click **+** next to the text that you entered.

5. Paste the following text in the file:

   ```md
   # Git Conventions
   When asked to commit on git, creating issues or PRs, use conventional commit messages in the form of `<type>: <description>`.
   Where:
   - `type` is one of: `fix`, `feat`, `build`, `chore`, `ci`, `docs`, `style`, `refactor`, `perf`, `test`.
   - `description` is a short description of the changes introduced in the commit, a summary of the issue or the PR.
   ```

6. Go to Agentforce Vibes prompts, paste this text then hit <kbd>Enter</kbd>:

   ```
   Commit my changes.
   ```

> [!TIP]
> Note how the rule that we've set up is used to format the commit message.

---

<p align="center">
   <a href="2-vibe-code-a-component.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="4-work-with-workflows.md">Next Exercise ▶︎</a>
</p>