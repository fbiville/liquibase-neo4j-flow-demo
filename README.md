<p align="left">
  <img src="img/liquibase.png" alt="Liquibase Logo" title="Liquibase Logo" width="324" height="72">
</p>

This repository contains a Liquibase and Neo4j demo. It is based off our standard demo, minus pre-validate. Liquibase licenses Neo4j by database.

The demo uses Docker. The lib files required for Neo4j are stored in the repo and mounted to /liquibase/lib at execution time.

# Pre-Demo Steps
1. Pull the repo to ensure you have all available updated files<br>
     ```
     git pull
     ```

# Demo Steps
1. **Quality Checks**
    1. Changeset "make-country-names-typed" in the [changelog file](Changesets/changelog.neo4j.xml) is missing a label.
    1. Running "Liquibase Workflow" executes the flow. Be sure "Quality Checks" is set to "T" in the dropdown.
    1. Once the job fails, add labels and check it back into GitHub (CLI or Editor).<br>
    ```
       git pull
       git commit -am "Add label"
       git push
    ```
1. **Flows**
    1. Rerun "Liquibase Workflow". 8 changes should be applied.
    1. The [flow file](liquibase.flowfile.yaml) works similar to our standard demo (i.e., Validate, Checks Show, Checks Run, etc.).
    1. Update and Quality Check reports are enabled by default.
    1. To show the reports, pull the repo.

# Reset
Execute the following steps to ready the environment for the next demo.
1. Run Liquibase Reset
1. Pull the repo
```
git pull
```
3. Remove the label from changeset "make-country-names-typed".

```
git commit -am "Reset files"
git push
```

# Contact Liquibase
#### Liquibase sales: https://www.liquibase.com/contact
#### Liquibase support: https://support.liquibase.com/knowledge
