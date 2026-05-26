---
name: scanning-org-security-quality
description: Scans the entire Org's codebase for potential security issues and code quality improvements using Salesforce Code Analyzer.
---

# scanning-org-security-quality

Retrieves the current Org's metadata (Apex classes, Apex triggers, LWCs, Aura components, Flows) locally using the Salesforce CLI and runs Salesforce Code Analyzer (SFCA) to inspect the project files for potential security issues and code quality improvements.

## Usage

Run this skill when the user requests a security, performance or quality audit for an org.
Never consider previous SFCA scan results as they could be outdated. Always run a fresh scan by following the steps below.

## Steps

Follow these exact steps:

1. Check if the project already contains a `sfca-results.csv` file at its root.

    If the file is present, asks for the permission to remove it before proceeding with the next steps.
    If the user rejects the request to delete it, abort the process.

2. Run this Salesforce CLI command to retrieve the org's metadata:

    ```sh
    sf project retrieve start -m ApexClass -m ApexTrigger -m LightningComponentBundle -m Flow -m AuraDefinitionBundle
    ```

3. Check if the SFCA CLI plugin (`code-analyzer`) is installed by running:

    ```sh
    sf plugins
    ```

    If the SFCA plugin is not installed, install it using:

    ```sh
    sf plugins install code-analyzer
    ```

4. Check if this project has a custom [Salesforce Code Analyzer YAML configuration file](https://developer.salesforce.com/docs/platform/salesforce-code-analyzer/guide/config-custom.html).

    First, look for common SFCA config filenames at the project root: `code-analyzer.yml` or `.code-analyzer.yml`. If not found there, inspect the `package.json` file for a script that references an SFCA configuration file, then check any YAML files it points to.

    We'll use `SFCA_CONFIG_PATH` to designate the path of the custom SFCA configuration file.

5. Inspect the `sfdx-project.json` file and determine the project's main package directory.

    We'll use `METADATA_PATH` to designate the path of this directory.

6. Run SFCA scoped to the retrieved metadata:

    ```sh
    sf code-analyzer run --workspace METADATA_PATH --view detail --output-file "sfca-results.csv"
    ```

    If the project has a custom SFCA configuration, add the following option to the command:

    ```sh
     --config-file SFCA_CONFIG_PATH
    ```

7. Parse `sfca-results.csv` and present the user with a summary:

    - Total number of violations found
    - Breakdown by severity (Critical, High, Medium, Low)
    - Breakdown by category (e.g., Security, Performance, Best Practices)
    - List the top Critical and High findings with their file location and a short description
