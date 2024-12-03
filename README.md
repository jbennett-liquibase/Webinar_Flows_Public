<p align="left">
  <img src="img/liquibase.png" alt="Liquibase Logo" title="Liquibase Logo" width="324" height="72">
</p>

This repository contains the demo scenarios for the "Liquibase 101" webinar originally delivered on December 19th, 2024. Recordings of all webinars can be found [here](https://www.liquibase.com/videos).

The demo is configured to use Docker, ADO public and GitHub Actions local runners, and on premise and cloud databases.

Note: public runners may not work for your ADO account until a request is made [here](https://forms.office.com/pages/responsepage.aspx?id=v4j5cvGGr0GRqy180BHbR5zsR558741CrNi6q8iTpANURUhKMVA3WE4wMFhHRExTVlpET1BEMlZSTCQlQCN0PWcu&route=shorturl) and Microsoft approves it. Monthly usage can be checked [here](https://dev.azure.com/sales-engineers/_settings/buildqueue?_a=concurrentJobs).

# Pre-Demo Steps
1. A [service connection](https://learn.microsoft.com/en-us/azure/devops/pipelines/library/service-endpoints?view=azure-devops) is required to access ADO resources. Once created, the connection must be granted the "Key Vault Administrator" and "Liquibase Operators" roles.
1. Pull the repo to ensure you have all available updated files<br>
     ```
     git pull
     ```

# Required ADO Variables
After forking this repository, set the following ADO pipeline variables or Azure Key Vault entries. This demo is configured to use Azure Key Vault.
|Variable |Description|
|----------|------------|
| LIQUIBASE_DEV_URL | The [JDBC URL](https://portal.azure.com/#@bizsparkdatical.onmicrosoft.com/resource/subscriptions/a38e082e-9dfc-49dd-a5e8-9d13e908b010/resourceGroups/jbennett-demo/providers/Microsoft.Sql/servers/jbdemo/databases/AdventureWorks2019/connectionStrings) of the target database.
| LIQUIBASE_DEV_USER | The database user.
| LIQUIBASE_DEV_PASSWORD | The database password.
| LIQUIBASE_KEY | A valid Liquibase license key.
| LIQUIBASE_REPO_TOKEN | A GitHub token used to access the respository.

# Required GitHub Variables
This demo is configured to use AWS Secrets Manger for credentials (see workflows for the variable settings). After forking this repository, set the following GitHub Actions secrets.
|Variable |Description|
|----------|------------|
| AWS_ACCESS_KEY_ID | AWS access key.
| AWS_SECRET_ACCESS_KEY | AWS secret access key.
| AWS_REGION | AWS region where secrets live (e.g., us-east-1).

# Demo Steps
1. **Liquibase OSS**
    1. Run "Liquibase OSS" in ADO. 6 changes should be applied (including delete w/o where)
1. **Liquibase Flow**
    1. Run "Liquibase Workflow" in ADO and GitHub Actions. Note flow is running same in Linux and Windows.

# Reset
Execute the following steps to ready the environment for the next demo.
1. Run Liquibase Reset
1. Pull the repository
```
git pull
```
3. Add changeset "dml_delete_businessunit" back to [changelog file](Changesets/changelog.mssql.sql) and update the repository
```
--changeset jbennett:dml_delete_businessunit labels:jira-1491,release-1.0.2
DELETE FROM Sales.BusinessUnit;
--rollback empty
```

```
git commit -am "Reset files"
git push
```

## Contact Liquibase
* Liquibase sales: https://www.liquibase.com/contact
* Liquibase support: https://support.liquibase.com