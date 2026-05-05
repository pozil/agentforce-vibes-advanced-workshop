# Exercise 1: Launch and Configure Agentforce Vibes

<p align="center">
   <a href="../README.md">▲ Home</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="2-vibe-code-a-component.md">Next Exercise ▶︎</a>
</p>

In this exercise, you'll launch Agentforce Vibes and configure it for the workshop.


## Step 1: Launch Agentforce Vibes IDE

1. Open the **Setup Menu** and click **Agentforce Vibes**.

   ![Screenshot showing the Setup menu with Agentforce Vibes](../assets/1-launch.jpg)

2. Accept the **Terms and Conditions**.

   ![Screenshot showing the Agentforce Vibes terms and conditions](../assets/1-terms.jpg)

> [!NOTE]
> It will take a few minutes for Agentforce Vibes to fully initialize. A Salesforce DX project will be automatically created for you and your org will be authorized by default.

> [!NOTE]
> You may see a large number of notifications in the bottom right of the IDE. This is where any IDE or Extension notifications will be published. You can close any that have appeared on launch.

3. The **Agentforce Sidebar** should be open by default, if it is not you can select the **Agentforce Vibes Icon** in the sidebar to open.

4. Select **I agree to the terms** and click **Enable and Start Building**.

   ![Screenshot showing a prompt to accept terms before enabling Agentforce Vibes](https://raw.githubusercontent.com/pozil/agentforce-vibes-advanced-workshop/main/assets/1-meet-agentforce.jpg)


### Step 2: Update the Salesforce DX MCP Servers

1. In the Agentforce Vibes Sidebar, Click **Manage MCP Servers**.

   ![Screenshot showing how to disable MCP servers](../assets/1-manage-mcp-servers.jpg)

2. Toggle off the **Salesforce API Context** and **Salesforce Metadata Experts** MCP servers. We will only use the Salesforce DX server for the workshop.

   ![Screenshot showing how to disable MCP servers](../assets/1-disable-mcp-servers.jpg)

3. Click the **Configuration Icon**.

   ![Screenshot showing the edit icon for MCP servers](../assets/1-edit-mcp-servers-icon.jpg)

4. Expand the **Salesforce DX** MCP server to take a look at the various tools that are enabled.

   ![Screenshot showing the Salesforce DX MCP server tools](../assets/1-salesforce-dx-tools.jpg)


## Step 3: Configure safe commands

1. From the **Agentforce Vibes Sidebar**, click **Auto-approve: Read, Edit, Safe Commands, MCP**

2. Click **Manage Safe Command Allow List** to open the configuration file (`a4d_safe_commands`).

   ![Screenshot showing the auto approval configuration panel](../assets/1-manage-safe-commands.png)

3. Paste the following lines at the end of the file:

   ```
   git status
   mkdir ...
   ls ...
   find ...
   head ...
   ```

---

<p align="center">
   <a href="../README.md">▲ Home</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="2-vibe-code-a-component.md">Next Exercise ▶︎</a>
</p>
