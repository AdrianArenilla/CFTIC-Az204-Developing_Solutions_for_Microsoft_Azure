# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 03: Retrieving Azure Storage resources and metadata by using the Azure Storage SDK for .NET
In this lab we will learn how to containerize and upload blobs using the Azure portal, enumerate blobs and containers with the Microsoft Azure Storage SDK for .NET and extract blob metadata with the Storage SDK.

### [Go to lab instructions -->](Files/AZ-204_03_lab.md)

## Working Architecture
![architecture03](architecture_03.png)

Create a storage account.
![](Evidences/Image1.png)


Create storage account containers.
![](Evidences/Image2.png)


Upload a blob into a container.
![](Evidences/Image3.png)


Enter the following command to create a new .NET project named BlobManager in the current folder:
```
dotnet new console --name BlobManager --output .
```
![](Evidences/Image4.png)


Enter the following command to import Azure.Storage.Blobs from NuGet:
```
dotnet add package Azure.Storage.Blobs
```
![](Evidences/Image5.png)


Enter the following command to build the .NET web application:
```
dotnet build
 ```
![](Evidences/Image6.png)


Modify the Program class to access Storage.
![](Evidences/Image7.png)


Enter the following command to run the .NET web application:
```
dotnet run
```
![](Evidences/Image8.png)


Update Program class to enumerate the existing containers.
![](Evidences/Image9.png)


Enter the following command to run the .NET web application:
```
dotnet run
```
![](Evidences/Image10.png)


Update de Program class to enumerate the blobs in an existing container by using the SDK and enter the following command to run the .NET web application:
```
dotnet run
```
![](Evidences/Image11.png)


Update de Program class to create a new container by using the SDK and enter the following command to run the .NET web application:
```
dotnet run
```
![](Evidences/Image12.png)


In the Containers section, we have the newly created vector graphics container.
![](Evidences/Image13.png)


Upload a new blob by using the portal.
![](Evidences/Image14.png)


Update the Program class to create an access blob URI by using the SDK and enter the following command to run the .NET web application:
```
dotnet run
```
![](Evidences/Image15.png)


We access the updated URL to access the online blob.
![](Evidences/Image16.png)


Enter the following command to delete the StorageMedia resource group:
```
az group delete --name StorageMedia --no-wait --yes
```
![](Evidences/Image17.png)


### [<-- Back to readme](../../../../)


