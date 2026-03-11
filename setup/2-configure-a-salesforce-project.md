# Exercise 2: Configure a Salesforce Project

[Back to home](../README.md)

In this Exercise, you'll configure your Salesforce project so that you can begin Vibe Coding with context.

## Step 1: Configure Your Project

1. Open the **Integrated Terminal** (press `` CTRL+` `` on both Mac and Windows)

1. Run the following command:

   ```shell
   sf project retrieve start -m CustomObject:Account -m CustomObject:Lead -m CustomObject:Opportunity CustomObject:Lead -m LightningComponentBundle:genericPageHeader -m PermissionSet:Partner_Management
   ```

   This command retrieves the following metadata:
   - Objects:
      - Account
      - Lead
      - Opportunity
   - `genericPageHeader` LWC
   - Partner Management permission set

> [!TIP]
> As an alernative to the CLI you can also retrieve the metadata manually with the Org Explorer.

> [!TIP]
> Downloading the objects ensures Agentforce Vibes can analyze your org’s schema and accurately generate Apex and LWC code.

3. Confirm your project folder includes:
   - Account, Lead, and Opportunity objects
   - The genericPageHeader LWC
   - Partner Management permission set

Your project is now fully configured with the metadata Agentforce Vibes needs to plan and generate the Partner Performance Dashboard.
