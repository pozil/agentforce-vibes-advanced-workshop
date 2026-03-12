# Exercise 2: Vibe Code a Component

<p align="center">
   <a href="1-launch-and-setup.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="3-work-with-rules-workflows-skills.md">Next Exercise ▶︎</a>
</p>

---

In this exercise, you'll configure your Salesforce project to retrieve some context and vibe code a component with a mutlimodal prompt.

## Step 1: Retrieve the Org's Metadata

1. Open the **Terminal** (press <kbd>CTRL</kbd> + <kbd>`</kbd> on both Mac and Windows)

1. Run the following command:

   ```shell
   sf project retrieve start -m CustomObject:Account -m CustomObject:Lead -m CustomObject:Opportunity CustomObject:Lead -m PermissionSet:Partner_Management
   ```

   This command retrieves the metadata required for the project.

> [!IMPORTANT]
> Downloading the objects ensures Agentforce Vibes can analyze your org’s schema and accurately generate Apex and LWC code.

> [!TIP]
> As an alernative to the CLI you could also retrieve the metadata manually with the Org Explorer.

3. Confirm that your project's `force-app/main/default` folder includes:
   - The **Account**, **Lead**, and **Opportunity** objects in the `objects` folder
   - The **Partner Management** permission set in the `permissionsets` folder

Your project is now fully configured with the metadata Agentforce Vibes needs to plan and generate the Partner Performance Dashboard.

## Step 2: Create a component with a multimodal prompt

In this step, we're going to use a multimodal prompt with an image to generate a component.

This is the hand drawn sketch that we'll use:

   ![UI sketch](../assets/2-ui-sketch.jpg)

1. Run the following command in the terminal to retrieve the image file in your project:

   ```shell
   curl -L -o ui-sketch.jpg \
   "https://agentforce-vibes-workshop.s3.us-east-2.amazonaws.com/agentforce-workshop-helper-1.0.0.vsix"
   ```

> [!TIP]
> The above step is specific to Agentforce Vibes IDE. With VS Code, the image can be located anywhere.

2. TODO

---

<p align="center">
   <a href="1-launch-and-setup.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="3-work-with-rules-workflows-skills.md">Next Exercise ▶︎</a>
</p>
