#Game Store API


##Starting Sql Server

```PowerShell

$sa_password = "[SA Password Here]"
docker run --memory 200m -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=$sa_password" -p 1433:1433 -v sqlvolume:/var/opt/mssql -d --rm --name mssql mcr.microsoft.com/mssql/server:2022-latest
```


## Setting the Connection String to Secret Manager
```Powershell
$sa_password = "[SA Password Here]"
dotnet user-secrets set "ConnectionStrings:GameStoreContext" "Server= localhost; Database=GameStore; User Id=sa; Password= $sa_password; TrustServerCertificate= True"
```#   G a m e _ S t o r e _ A p i  
 