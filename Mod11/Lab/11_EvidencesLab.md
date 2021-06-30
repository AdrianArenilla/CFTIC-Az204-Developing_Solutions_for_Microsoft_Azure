# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 11: Asynchronously processing messages by using Azure Queue Storage
In this lab we will learn how to add Azure.Storage libraries from NuGet, create a queue in .NET, generate a new message in the queue using .NET, consume a message from the queue using .NET, and manage a queue using Azure Storage Explorer.

### [Go to lab instructions -->](Files/AZ-204_11_lab.md)

## Working Architecture
![architecture11](architecture_11.png)

Create a storage account.
![](Evidences/Image1.png)


Enter the following command to create a new .NET project named MessageProcessor in the current folder:
```
dotnet new console --name MessageProcessor --output .
```
![](Evidences/Image2.png)


Enter the following command to import *Azure.Storage.Queues from NuGet:
```
dotnet add package Azure.Storage.Queues
```
![](Evidences/Image3.png)


Enter the following command to build the .NET web application:
```
dotnet build
```
![](Evidences/Image4.png)


Update the Program class and enter the following command to run the .NET web application:
```
dotnet run
```
![](Evidences/Image5.png)


Update the Program class and enter the following command to run the .NET web application:
```
dotnet build
```
![](Evidences/Image6.png)


Enter the following command to run the .NET web application:
```
dotnet run
```
![](Evidences/Image7.png)


Open Azure Storage Explorer.
![](Evidences/Image8.png)


Add a message into Azure Storage Explorer.
![](Evidences/Image9.png)


Test message queue access. Enter the following command to run the .NET web application:
```
dotnet run
```
![](Evidences/Image10.png)


Update the Program class to delete queue messages.
![](Evidences/Image11.png)


View deleted queued messages using Storage Explorer.
![](Evidences/Image12.png)


Update the Program class to create queue new messages by using .NET. Enter the following command to run the .NET web application:
```
dotnet run
```
![](Evidences/Image13.png)


View queued messages by using Storage Explorer.
![](Evidences/Image14.png)


Enter the following command to delete the AsyncProcessor resource group:
```
az group delete --name AsyncProcessor --no-wait --yes
```
![](Evidences/Image15.png)


### [<-- Back to readme](../../readme.md)


