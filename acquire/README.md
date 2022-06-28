# Extracting data

The data extraction goes in this folder. A common workflow is a set of SQL scripts which each generate a table. A shell script iterates through each generating the tables on a BigQuery dataset. Once ready, each dataset is exported to GCS, and either used in the cloud or downloaded locally for analysis.

Separating the cohort and covariate code into a separate folders is helpful for organizing the code, but it is by no means required.

## Setup with GCP

## Create a Google Cloud Storage (GCS) bucket for exporting data

## Create a BigQuery dataset for results

## Write stand-alone queries which generate tables

## Run the generate_tables.sh script

## Add GCP credentials to GitHub

## Update GitHub workflow (if necessary)

## Make a release which triggers a build of the tables