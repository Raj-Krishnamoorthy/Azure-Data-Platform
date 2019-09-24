Running SQL Server 2019 on ACI - Azure Container Instance through Powershell

Pre-requisite


Azure Portal subscription

Powershell 6.x  ( https://docs.microsoft.com/en-us/powershell/azure/new-azureps-module-az?view=azps-2.7.0)


Step 1:  Create resource group





![image](https://user-images.githubusercontent.com/49286341/65555775-574ab600-dee2-11e9-972f-13c5bd68ca21.png)



Step 2 : Creating the sql server image on linux for Docker 
(https://hub.docker.com/_/microsoft-mssql-server)


![image](https://user-images.githubusercontent.com/49286341/65555781-5b76d380-dee2-11e9-809f-354c49a7d542.png)



![image](https://user-images.githubusercontent.com/49286341/65555789-67fb2c00-dee2-11e9-8870-8f4720bbb0f9.png)


Output on both command line & the portal for confirmation screen


![image](https://user-images.githubusercontent.com/49286341/65555813-7a756580-dee2-11e9-87e5-727239b8e8d3.png)



![image](https://user-images.githubusercontent.com/49286341/65555835-8b25db80-dee2-11e9-8e1b-858a0daae1d6.png)


PS C:\> az container logs --resource-group dockerACIRG --name mssql-2019

Output/tail end screenshot


![image](https://user-images.githubusercontent.com/49286341/65555857-9bd65180-dee2-11e9-86cd-2257a47c2d78.png)



CONNECTING TO SQL via SQLCMD


![image](https://user-images.githubusercontent.com/49286341/65555889-ac86c780-dee2-11e9-921c-d38e3db46250.png)


Creating test database

![image](https://user-images.githubusercontent.com/49286341/65555892-b0b2e500-dee2-11e9-8565-97cfc870dd16.png)


![image](https://user-images.githubusercontent.com/49286341/65555897-b4df0280-dee2-11e9-89e8-e470068e516c.png)


AUTOMATION PART : Click on the EXPORT TEMPLATE on the left panel & click on the ADD TO LIBRARY on the top


![image](https://user-images.githubusercontent.com/49286341/65555922-c7593c00-dee2-11e9-8e41-40ec6a3fc94c.png)


Save the template by clicking add to library & CLICK DEPLOY

![image](https://user-images.githubusercontent.com/49286341/65555925-cc1df000-dee2-11e9-85db-d7e6261f0734.png)


EDIT TEMPLATE based on your requirement. In this example changed the name to mssql-2019-v2 from mssql-2019.

Agree to the terms & CLICK PURCHASE


![image](https://user-images.githubusercontent.com/49286341/65555935-d17b3a80-dee2-11e9-8005-8e8cbbaeb1fa.png)



CLEANING UP - Deleting my original resource group


![image](https://user-images.githubusercontent.com/49286341/65555951-d63fee80-dee2-11e9-83b5-81f8c92d61e3.png)
