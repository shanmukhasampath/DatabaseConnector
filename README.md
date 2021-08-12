DatabaseConnector
=================

This is a mirror of https://github.com/OHDSI/DatabaseConnector. 

With a modification to make it to work into FinnGen's SandBox. 

Concretely, we added the possibility to connect with bigrquery-DBI wich is the driver used in the SandBox. 




```r
bq_auth(scopes="https://www.googleapis.com/auth/bigquery.readonly")

connectionDetails_bq_dbi <- DatabaseConnector::createConnectionDetails(
  dbms = "bigquery-dbi",
  bq_dbi_project = "finngen-production-library",
  bq_dbi_dataset = "finngen_omop",
  bq_dbi_billing = "fg-production-sandbox-4" #replace this with your sandbox name (check link in browser)
)


conn_bq_dbi <- DatabaseConnector::connect(connectionDetails_bq_dbi)

conn_bq_dbi
```

