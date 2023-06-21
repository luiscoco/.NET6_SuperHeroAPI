# .NET6_SuperHeroAPI
The detailed video explaning the code is in the URL: https://www.youtube.com/watch?v=dtthbiP3SE0

1.Open the appsettings.json and set the server name to localhost or to .
```json
{
  "ConnectionStrings": {
    "DefaultConnection" : "server=.;database=superherodb;trusted_connection=true"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*"
}
```

2.Copy the dtabase name in the appsettings.json and open SSMS (SQL Server Management Studio).
Create a new database in SSMS with the name "superherodb" as specified in appsettings.json file.

```sql
create database superherodb
go
```

3.Open the Package Manager PM in Visual Studio and apply the database migration. 
In PM run the command. Be sure to select as Default Project the SuperHeroAPI.
```
Update-Database
```
For running this command it is mandatory to be installe the pacakage: Microsoft.EntityFrameworkCore.Tools

4.In Visual Studio build and run the application. Select the "SuperHeroAPI" option for running.
