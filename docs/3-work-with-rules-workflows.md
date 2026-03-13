# Exercise 3: Work with Rules and Workflows

<p align="center">
   <a href="2-vibe-code-a-component.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
</p>

---

In this exercise, you'll configure GitHub and work with [Rules](https://developer.salesforce.com/docs/platform/einstein-for-devs/guide/devagent-rules.html) and [Workflows](https://developer.salesforce.com/docs/platform/einstein-for-devs/guide/devagent-workflows.html) to automate actions with Agentforce Vibes and move your code to a repository.

## Step 1: Authenticate with GitHub

1. Run this command in the terminal to authenticate with GitHub:

   ```shell
   gh auth login --git-protocol https --hostname github.com --web
   ```

2. Type `yes` to confirm the authentication request.
3. Copy the one-time code from the command's output.
4. Press <kbd>Enter</kbd>.
5. Click **Open** to allow the redirection to github.com.
6. On the GitHub page, paste the one-time code and click **Continue**.
7. Click **Authorize GitHub**.
8. If prompted, enter your GitHub credentials.
9. Close the GitHub page and go back to Agentforce Vibes IDE.
10. Ensure that the last command ended with something like:

   ```
   ✓ Authentication complete.
   - gh config set -h github.com git_protocol https
   ✓ Configured git protocol
   ! Authentication credentials saved in plain text
   ✓ Logged in as pozil
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
> We've excluded our Apex and LWC code from the initial commit. We'll add them in a separate commit.


## Step 3: Create a rule for git work

1. From the **Agentforce Vibes Sidebar**, click the **Manage Agentforce Rules & Workflows** (balance) icon:

   ![Icon for Manage Agentforce Rules & Workflows](../assets/3-rules-icon.png)

2. Make sure that you're on the **Rules** tab.

3. Enter `custom-git-convention.md` under the **Workspace Rules** section.

4. Click **+** next to the text that you entered.

5. Paste the following text in the file:

   ```md
   # Git Conventions
   When asked to commit on git, creating issues or PRs, use conventional commit messages in the form of `<type>: <description>`.
   Where:
   - `type` is one of: `fix`, `feat`, `build`, `chore`, `ci`, `docs`, `style`, `refactor`, `perf`, `test`.
   - `description` is a short description of the changes introduced in the commit, a summary of the issue or the PR.
   ```

## Step 4: Create a workflow to manage GitHub releases



---

<p align="center">
   <a href="2-vibe-code-a-component.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
</p>