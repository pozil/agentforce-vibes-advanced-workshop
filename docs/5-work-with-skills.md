# Exercise 5: Work with Skills

<p align="center">
   <a href="4-work-with-workflows.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="6-migrate-from-aura-to-lwc.md">Next Exercise ▶︎</a>
</p>

---

In this exercise, you'll create a custom [Agentforce Vibes Skill](https://developer.salesforce.com/docs/platform/einstein-for-devs/guide/skills.html) that helps with checking your org for security and quality best practices using [Salesforce Code Analyzer](https://developer.salesforce.com/docs/platform/salesforce-code-analyzer/guide).

> [!NOTE]
> The Salesforce DX MCP server contains Salesforce Code Analyzer tools for scanning a couple of specific local files. This skill lets you scan the entire org's codebase in a well-defined process.

## Step 0: Scan the org without a custom skill (optional)

1. Run the following prompt:

   ```
   Inspect my org for security and quality best practices.
   ```

2. Accept the different commands that the agent offers to run.

3. Notice the following limitations:
   - the agent struggles to pass the right parameters to the `run_code_analyzer` tool and needs a couple of attempts to get this right.
   - only a subset of local files are scanned.



## Step 1: Create a custom skill

1. From the **Agentforce Vibes Sidebar**, click the **Manage Agentforce Rules & Workflows** (balance) icon.

2. Click the **Skills** tab.

3. Enter `scanning-org-security-quality` under the **Workspace Skills** section and click **+**.

4. Replace the entire content of the `SKILL.md` file with [this content](https://raw.githubusercontent.com/pozil/agentforce-vibes-advanced-workshop/main/assets/scanning-org-security-quality.md).

5. Save the file.

## Step 2: Test your custom skill

1. Run the same prompt as in Step 0:

   ```
   Inspect my org for security and quality best practices.
   ```

2. Notice in the agent's response that the `scanning-org-security-quality` skill is being used.

3. Accept the different commands that the agent offers to run.

4. At the end of the execution, you'll get a list of rule violations with some recommendations for the entire org. Note the high severity violations for the `superSort.cls` Apex file that weren't detected when the prompt was first run without the skill.

---

<p align="center">
   <a href="4-work-with-workflows.md">◀︎ Previous Exercise</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="../README.md">▲ Home</a>
   &nbsp;<b>|</b>&nbsp;
   <a href="6-migrate-from-aura-to-lwc.md">Next Exercise ▶︎</a>
</p>