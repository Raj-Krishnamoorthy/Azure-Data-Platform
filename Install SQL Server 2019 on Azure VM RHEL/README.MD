How to install SQL SERVER 2019 (developer version) Installation on RedHat linux on Azure.

Pre-requisite
 Azure subscription
 
Atleast 2 GB of RAM for the VM. In this example, I have used A2 V2 (2 vcpus, 4 GiB mem)

Screenshots attached.
![image](https://user-images.githubusercontent.com/49286341/64213583-61890f80-ce62-11e9-904e-08a6c042402c.png)


![image](https://user-images.githubusercontent.com/49286341/64213588-651c9680-ce62-11e9-8487-0541b32446c3.png)




![image](https://user-images.githubusercontent.com/49286341/64213603-6d74d180-ce62-11e9-805e-dd80a52c837b.png)


![image](https://user-images.githubusercontent.com/49286341/64213609-72398580-ce62-11e9-9aa8-249d696dce0d.png)


![image](https://user-images.githubusercontent.com/49286341/64213617-7a91c080-ce62-11e9-9970-567c94db58d4.png)


![image](https://user-images.githubusercontent.com/49286341/64213627-81b8ce80-ce62-11e9-93a6-37711acb502c.png)

Check for SQL Server Status


![image](https://user-images.githubusercontent.com/49286341/64213640-8bdacd00-ce62-11e9-9d55-4eecfcc86e21.png)


Enable 1433 port for the firewall

![image](https://user-images.githubusercontent.com/49286341/64213690-97c68f00-ce62-11e9-8450-588d1cc04355.png)


RedHat repo config file

![image](https://user-images.githubusercontent.com/49286341/64213699-a0b76080-ce62-11e9-9ce3-3c1aab637ae3.png)


Install MS-SQL Tools

![image](https://user-images.githubusercontent.com/49286341/64213707-aa40c880-ce62-11e9-8c5d-c0e062239b1b.png)


Before modifying bash_profile & bash_rc , here is the content & next screenshot shows backing up the original files


![image](https://user-images.githubusercontent.com/49286341/64213771-e6742900-ce62-11e9-87ba-31839bd70aad.png)


![image](https://user-images.githubusercontent.com/49286341/64213775-eaa04680-ce62-11e9-9945-953a6a3b8349.png)

Add /opt/mssql-tools/bin to PATH in bash_profile & bash_rc. Then validating the path through env command

![image](https://user-images.githubusercontent.com/49286341/64213820-0ad00580-ce63-11e9-903a-97b73a94ef2a.png)


Connect locally to the SQL Server DB

![image](https://user-images.githubusercontent.com/49286341/64213832-13c0d700-ce63-11e9-9dcc-352f36223f18.png)

You can also connect via SSMS from your client machine or laptop to this database by using the server name from the overview page of Azure portal and make sure 1433 port is open.
