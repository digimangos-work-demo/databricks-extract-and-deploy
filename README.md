# PoC to migrate Databricks config

This PoC project is designed to export configuration from Databricks and commit it to the repository. It can then also deploy to a separate environment.

## Configuration

For this PoC you need to configure two environments:

  - `Dev` - Used for extracting configuration
  - `QA` - Used for deploying configuration
	
Both of these environments require some configuration of a secret and a variable:

Environment variable:
  - `DATABRICKS_HOST` - Containing the URL to the databricks host i.e. https://adb-1234567890.1.azuredatabricks.net
	
Secret:
  - `DATABRICKS_PAT` - PAT token to authenticate with databricks server.
	
## Actions

After configuration, two workflows will exist on the Actions tab. These are both started using a manual `workflow-dispatch`

