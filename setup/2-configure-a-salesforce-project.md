# Exercise 2: Configure a Salesforce Project

[Back to home](../README.md)

In this Exercise, you'll configure your Salesforce project so that you can begin Vibe Coding with context.

## Step 1: Configure Your Project

1. Open the **Terminal** (press `` CTRL+` `` on both Mac and Windows)

1. Run the following command:

   ```shell
   sf project retrieve start -m CustomObject:Account -m CustomObject:Lead -m CustomObject:Opportunity CustomObject:Lead -m LightningComponentBundle:genericPageHeader -m PermissionSet:Partner_Management
   ```

   This command retrieves the metadata required for the project.

> [!TIP]
> As an alernative to the CLI you could also retrieve the metadata manually with the Org Explorer.

> [!IMPORTANT]
> Downloading the objects ensures Agentforce Vibes can analyze your org’s schema and accurately generate Apex and LWC code.

3. Confirm that your project's `force-app/main/default` folder includes:
   - The **Account**, **Lead**, and **Opportunity** objects in the `objects` folder
   - The `genericPageHeader` LWC in the `lwc` folder
   - The **Partner Management** permission set in the `permissionsets` folder

Your project is now fully configured with the metadata Agentforce Vibes needs to plan and generate the Partner Performance Dashboard.
