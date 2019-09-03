+How to migrate Azure SQL DB serverless to Provisioned compute tier.

Installation

Create an Azure sql database from the portal, CLI or PowerShell and choose Serverless option ( GEN 5)

Minimum Vcore 2 during this creation.

Open the Azure SQL firewall from the portal, CLI or PowerShell

Using Azure Powershell(6.x) to migrate Serverless tier to Provisioned tier.


Powershell command to migrate serverless to provisioned compute tier

Set-AzSqlDatabase -ResourceGroupName "servrless-resgp" -DatabaseName "sqldb01" -ServerName "serverless01" -ComputeModel Provisioned -ComputeGeneration Gen5 
