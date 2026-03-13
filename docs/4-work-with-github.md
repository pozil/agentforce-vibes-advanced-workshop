# Exercise 4: Work with GitHub

<p align="center">
   <a href="3-work-with-rules-workflows-skills.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
</p>

---

In this exercise, you configure GitHub and move your code to a repository.


## Step 1: Authenticate with GitHub

1. Run this command in the terminal to authenticate with GitHub:

   ```shell
   gh auth login --git-protocol https --hostname github.com --web
   ```

1. Type `yes` to confirm the authentication request
1. Copy the one-time code from the command's output.
1. Press <kbd>Enter</kbd>.
1. Click **Open** to allow the redirection to github.com.
1. On the GitHub page, paste the one-time code and click **Continue**.
1. Click **Authorize GitHub**.
1. If prompted, enter your GitHub credentials.
1. Close the GitHub page and go back to Agentforce Vibes IDE.
1. Ensure that the last command ended with something like:

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

1. Run these commands in the terminal to initialize a local git repository and create an initial commit:

   ```shell
   git init
   git add .
   git commit -m "feat: initial commit"
   ```

---

<p align="center">
   <a href="3-work-with-rules-workflows-skills.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
</p>