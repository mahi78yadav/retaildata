Create datalake prompt:
----------------------
Build an Azure Databricks Retail Data Lakehouse project.

**Source:** https://github.com/mahi78yadav/retaildata/tree/main/Data

**Azure Resources:**
- Resource Group: `mahi78retaildata_dev`
- Storage Account: `mahi78retaildatadev`
- Access Connector: `ac-retaildata_dev`

**Permissions:** Assign the following roles to the Access Connector's managed identity at storage account scope:
- Storage Blob Data Contributor
- Storage Account Access Contributor
- EventGrid Data Subscriber
- Storage Queue Data Contributor

Verify exact Azure role names before assignment.

**ADLS Gen2 Structure:**
```text
bronze/{customers,products,stores,orders}
silver/{customers,products,stores,orders}
gold/bt/
```

Create the containers and folders in the specified storage account.

Configure Databricks access using managed identity. Implement Bronze ingestion, Silver transformations and Gold aggregations using PySpark and Delta Lake. Follow Medallion Architecture and validate each implementation step.
