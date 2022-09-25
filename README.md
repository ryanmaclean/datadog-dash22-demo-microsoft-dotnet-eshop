# Dash 22 Dotnet Demo Documentation

Sample repo used for Dash 22 demos using Microsoft Dotnet and Azure App Service + Azure SQL

# Metrics
Metrics to Use in Datadog (click `<>`):

Azure SQL Queries: `sum:sqlserver.queries.count{name:eshop}.as_count()`

Azure SQL Storage: `avg:azure.sql_servers.storage_used{*} by {kind,name,env}`
