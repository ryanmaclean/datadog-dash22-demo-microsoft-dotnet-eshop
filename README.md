# Dash 22 Dotnet Demo Documentation

Sample repo used for Dash 22 demos using Microsoft Dotnet and Azure App Service + Azure SQL.

Unless otherwise specified, this can all be done using Azure Cloud Shell: https://shell.azure.com/bash (fun fact, `zsh` works in that URL for some reason :D ). 

# Metrics to Use in Notebook
A JSON file for some simple queries are in the notebook, but some to use as tests to ensure the deployment worked are noted here. These test for the App Service deployments and Azure SQL deployment.

Metrics to Use in Datadog (click `<>`):
 * Azure SQL Queries: `sum:sqlserver.queries.count{name:eshop}.as_count()`
 * Azure SQL Storage: `avg:azure.sql_servers.storage_used{*} by {kind,name,env}`

# Terraform
There are a few Terraform bit in here, but they are not necessary if you'd rather use Bicep or Arm tempaltes (or maybe Arm templates with Terraform).

# Packer
You can also safely ignore the Packer files if you're alright building a Datadog Agent VM or soemthing else (container, K8S config) to handle the Azure SQL monitoring, or are OK with the agent being on a Windows-based SQL server. 

# Docs

[Build Windows images with Packer for Azure](https://learn.microsoft.com/en-us/azure/virtual-machines/windows/build-image-with-packer)
