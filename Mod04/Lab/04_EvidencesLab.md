# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 04: Constructing a polyglot data solution
In this lab we will learn how to instantiate multiple database services using the Azure portal, write C# code to connect to the SQL database and write C# code to connect to Azure Cosmos DB.

### [Go to lab instructions -->](Files/AZ-204_04_lab.md)

## Working Architecture
![architecture04](architecture_04.png)

Create an Azure SQL Database server resource.
![](Evidences/Image1.png)


Create an Azure Cosmos DB account resource.
![](Evidences/Image2.png)


Create an Azure Storage account resource.
![](Evidences/Image3.png)


Create storage account containers.
![](Evidences/Image4.png)


Upload a blob into a container.
![](Evidences/Image5.png)


Create storage account containers.
![](Evidences/Image6.png)


Upload a blob into a container.
![](Evidences/Image7.png)


Import an SQL database.
![](Evidences/Image8.png)


This step ensures that the local machine has access to the databases associated with this server.
![](Evidences/Image9.png)


Enter the following query to view all the data in the models table.
```
SELECT * FROM AdventureWorks.dbo.Models
```
![](Evidences/Image10.png)


Enter the following query to view all the data in the products table.
```
SELECT * FROM AdventureWorks.dbo.Products
```
![](Evidences/Image11.png)


Enter the following command to build the .NET web application:
```
dotnet build
```
![](Evidences/Image12.png)


Update the JSON file.
Enter the following command to switch your terminal context to the AdventureWorks.Web folder:
```
cd .\AdventureWorks.Web\
```

Enter the following command to run the .NET web application:
```
dotnet build
```
![](Evidences/Image13.png)


Go to the following address to see the result currently obtained (<http://localhost:5000>).
![](Evidences/Image14.png)


Go to the water bottle and visualize the result.
![](Evidences/Image15.png)


Enter the following command to create a new .NET console project named AdventureWorks.Migrate:
```
dotnet new console --name AdventureWorks.Migrate --framework netcoreapp3.1
```
![](Evidences/Image16.png)


Enter the following command to add a reference to the existing AdventureWorks.Models project:
```
dotnet add .\AdventureWorks.Migrate\AdventureWorks.Migrate.csproj reference .\AdventureWorks.Models\AdventureWorks.Models.csproj
```
![](Evidences/Image17.png)


Enter the following command to add a reference to the existing AdventureWorks.Context project:
```
dotnet add .\AdventureWorks.Migrate\AdventureWorks.Migrate.csproj reference .\AdventureWorks.Context\AdventureWorks.Context.csproj
```
![](Evidences/Image18.png)


First enter the following command to switch your terminal context to the AdventureWorks.Migrate folder:
```
cd .\AdventureWorks.Migrate\
```

After enter the following command to import Microsoft.EntityFrameworkCore.SqlServer from NuGet:
```
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
```
![](Evidences/Image19.png)


Enter the following command to import Microsoft.Azure.Cosmos from NuGet:
```
dotnet add package Microsoft.Azure.Cosmos
```
![](Evidences/Image20.png)


Enter the following command to build the .NET console application:
```
dotnet build
```
![](Evidences/Image21.png)


Update the Program class and enter the following command to switch your terminal context to the AdventureWorks.Migrate folder:
```
cd .\AdventureWorks.Migrate\
```
After enter the following command to build the .NET console application:
 ```
dotnet build
```
![](Evidences/Image22.png)


Update the Program class to get SQL database records by using Entity Framework and enter the following command to build the .NET console application:
```
dotnet build
```
![](Evidences/Image23.png)


Update the Program class to insert items into Azure Cosmos DB and enter the following command to build the .NET console application:
```
dotnet build
```
![](Evidences/Image24.png)


Enter the following command to perform a migration and run the .NET console application:
```
dotnet run
```
![](Evidences/Image25.png)


Enter the following command within the Azure Cosmos DB data explorer to view the results in the Azure portal:
```
SELECT * FROM models
```
![](Evidences/Image26.png)


Replace the existing text with the following text:
```
SELECT VALUE COUNT(1) FROM models
```
![](Evidences/Image27.png)


Enter the following command to import Microsoft.Azure.Cosmos from NuGet:
```
dotnet add package Microsoft.Azure.Cosmos
```
![](Evidences/Image28.png)


Enter the following command to build the .NET web application:
```
dotnet build
```
![](Evidences/Image29.png)


Update the AdventureWorksCosmosContext class to write .NET code to connect to Azure Cosmos DB and enter the following command to build the .NET web application:
```
dotnet build
```
![](Evidences/Image30.png)


Update the Startup class to update .NET application startup logic.
![](Evidences/Image31.png)


Validate that the .NET application successfully connects to Azure Cosmos DB.
![](Evidences/Image32.png)


Enter the following command to delete the PolyglotData resource group:
```
az group delete --name PolyglotData --no-wait --yes
```
![](Evidences/Image33.png)


### [<-- Back to readme](../../readme.md)


