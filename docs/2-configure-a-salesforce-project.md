# Exercise 2: Configure a Salesforce Project

<p align="center">
   <a href="1-launch-and-setup.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
</p>

---

In this Exercise, you'll configure your Salesforce project so that you can begin Vibe Coding with context.

## Step 1: Retrieve the Org's Metadata

1. Open the **Terminal** (press <kbd>CTRL</kbd>+<kbd>`</kbd> on both Mac and Windows)

1. Run the following command:

   ```shell
   sf project retrieve start -m CustomObject:Account -m CustomObject:Lead -m CustomObject:Opportunity CustomObject:Lead -m LightningComponentBundle:genericPageHeader -m PermissionSet:Partner_Management
   ```

   This command retrieves the metadata required for the project.

> [!IMPORTANT]
> Downloading the objects ensures Agentforce Vibes can analyze your org’s schema and accurately generate Apex and LWC code.

> [!TIP]
> As an alernative to the CLI you could also retrieve the metadata manually with the Org Explorer.

3. Confirm that your project's `force-app/main/default` folder includes:
   - The **Account**, **Lead**, and **Opportunity** objects in the `objects` folder
   - The `genericPageHeader` LWC in the `lwc` folder
   - The **Partner Management** permission set in the `permissionsets` folder

Your project is now fully configured with the metadata Agentforce Vibes needs to plan and generate the Partner Performance Dashboard.

---

<p align="center">
   <a href="1-launch-and-setup.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
</p>