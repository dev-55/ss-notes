# Solution Setup

## File Creation
```
dotnet new sln
dotnet new webapi -o API
dotnet sln add API

dotnet new classlib -o Core
dotnet sln add Core

dotnet new classlib -o Infrastructure
dotnet sln add Infrastructure

...Api> dotnet add reference ../Infrastructure
...Infrastructure> dotnet add reference ../Core

root> dotnet restore
```

&nbsp; 
## Certificates

Check for certificate with
```
dotnet dev-certs https
``` 

Trust this with 
```
dotnet dev-certs https -t
```

&nbsp; 
## Database Migrations

Install the EF CLI

    dotnet tool install --global dotnet-ef --version 3.1.1

		
Install NuGet package

    Microsoft.EntityFrameworkCore.Design


EF Commands

    dotnet ef -h

Create a Migration

    dotnet ef migrations add InitialCreate -o Data/Migrations
    dotnet ef migrations add InitialCreate -p Infrastructure -s Api -o Data/Migrations

Create the database

    dotnet ef database update

    Insert Data
        INSERT INTO `Entities` (Id, Name)
        VALUES 
            (1, 'Entity 1'),
            (2, 'Entity 2'),
            (3, 'Entity 3');
        
Remove a Migration

    dotnet ef migrations remove
    dotnet ef migrations remove -p Infrastructure -s Api

Downgrade a Database to a Previous Migration
    dotnet ef database update MigrationName
    or
    dotnet ef database update 0 (to go back to the start)


Drop the database
    dotnet ef database drop
    dotnet ef database drop -p Infrastructure -s Api


&nbsp; 
## Dependencies

### AutoMapper
Add NuGet package
```
AutoMapper.Extensions.Microsoft.DependencyInjection 
```
to Api Project

### Swagger
Add NuGet packages
```
    Swashbuckle.AspNetCore.SwaggerGen
    Swashbuckle.AspNetCore.SwaggerUI
```