+How to migrate Azure SQL DB serverless to Provisioned compute tier.

Installation

Create an Azure sql database from the portal, CLI or PowerShell and choose Serverless option ( GEN 5)

Minimum Vcore 2 during this creation.

Open the Azure SQL firewall from the portal, CLI or PowerShell

Using Azure Powershell(6.x) to migrate Serverless tier to Provisioned tier.


Powershell command to migrate serverless to provisioned compute tier

Set-AzSqlDatabase -ResourceGroupName "servrless-resgp" -DatabaseName "sqldb01" -ServerName "serverless01" -ComputeModel Provisioned -ComputeGeneration Gen5 


![image](https://user-images.githubusercontent.com/49286341/64207356-537ec300-ce51-11e9-906f-fb09eb911c2a.png)

![image](https://user-images.githubusercontent.com/49286341/64207367-55e11d00-ce51-11e9-8122-a2323d79527b.png)


![image](https://user-images.githubusercontent.com/49286341/64207373-5a0d3a80-ce51-11e9-8fc7-fc8b614e6758.png)


![image](https://user-images.githubusercontent.com/49286341/64207381-5da0c180-ce51-11e9-8d66-811ef4eb495d.png)


![image](https://user-images.githubusercontent.com/49286341/64207389-609bb200-ce51-11e9-8401-81516361e86f.png)


![image](https://user-images.githubusercontent.com/49286341/65351900-1aa75380-db9e-11e9-836a-bd997738624d.png)

after migration

![image](https://user-images.githubusercontent.com/49286341/65351865-fc415800-db9d-11e9-8dab-ee048fb755e1.png)
