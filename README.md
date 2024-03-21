<p align="left">
  <img src="img/liquibase.png" alt="Liquibase Logo" title="Liquibase Logo" width="324" height="72">
</p>

This repository contains a Liquibase and Snowflake demo. It is based off our standard demo, minus pre-validate. Liquibase licenses Snowflake by schema.

The demo uses Docker.

# Pre-Demo Steps
1. Pull the repo to ensure you have all available updated files<br>
     ```
     git pull
     ```

# Demo Steps
1. **Flows**
    1. Run "Liquibase Workflow". 8 changes should be applied.
    1. The [flow file](liquibase.flowfile.yaml) works similar to the demo environment (i.e., Validate, Checks Show, Checks Run, etc.).
    1. Update and Drift reports are enabled by default.
    1. To show the reports, pull the repo.
1. **Targeted Rollback**
    1. Run "Liquibase Targeted Rollback".
    1. The default values will rollback changeset 2.
    1. The history command is run once before the rollback and once after.

# Reset
Execute the following steps to ready the environment for the next demo.
1. Run Liquibase Reset
1. Pull the repo
```
git pull
```
3. Delete logs and reports and update the repository

```
git commit -am "Reset files"
git push
```

# Contact Liquibase
#### Liquibase sales: https://www.liquibase.com/contact
#### Liquibase support: https://support.liquibase.com/knowledge
