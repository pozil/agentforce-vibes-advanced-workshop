# Exercise 4: Work with Workflows

<p align="center">
   <a href="3-work-with-rules.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
</p>

---

In this exercise, you'll configure GitHub and work with [Workflows](https://developer.salesforce.com/docs/platform/einstein-for-devs/guide/devagent-workflows.html) to automate actions with Agentforce Vibes.


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

> [!TIP]
> You can run "gh auth status" to verify that you're correctly authenticated.


## Step 2: Create a workflow to manage GitHub releases



---

<p align="center">
   <a href="3-work-with-rules.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
</p>