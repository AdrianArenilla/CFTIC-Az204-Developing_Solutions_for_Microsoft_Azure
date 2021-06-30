# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 10: Publishing and subscribing to Event Grid events
In this lab we will learn how to create an Event Grid topic, use the Azure Event Grid viewer to subscribe to a topic, and illustrate published messages and publish a message from a .NET application.

### [Go to lab instructions -->](Files/AZ-204_10_lab.md)

## Working Architecture
![architecture10](architecture_10.png)

In Azure portal, at the Cloud Shell command prompt enter the following command to get the version of the Azure Command-Line Interface (Azure CLI) tool:
```
az --version
```
![](Evidences/Image1.png)


Enter the following command to list just the namespaces of the currently registered providers:
```
az provider list --query "[].namespace"
```
![](Evidences/Image2.png)


Review the list of currently registered providers. Notice that the Microsoft.EventGrid provider is currently included in the list of providers.
![](Evidences/Image3.png)


Create a custom Event Grid topic.
![](Evidences/Image4.png)


Deploy the Azure Event Grid viewer to a web app.
![](Evidences/Image5.png)


Access the Event Grid Viewer web application.
![](Evidences/Image6.png)


Observe the currently running Azure Event Grid viewer web application. 
![](Evidences/Image7.png)


Create new subscription.
![](Evidences/Image8.png)


Observe the subscription validation event in JSON format.
![](Evidences/Image9.png)


Enter the following command to create a new .NET project named EventPublisher in the current folder:
```
dotnet new console --name EventPublisher --output .
```
![](Evidences/Image10.png)


Enter the following command to import Azure.Messaging.EventGrid from NuGet:
```
dotnet add package Azure.Messaging.EventGrid
```
![](Evidences/Image11.png)


Enter the following command to build the .NET web application:
```
dotnet build
```
![](Evidences/Image12.png)


Update the Program class and enter the following command to run the .NET web application:
```
dotnet run
```
![](Evidences/Image13.png)


Observe published events in JSON format.
![](Evidences/Image14.png)


Enter the following command to delete the PubSubEvents resource group:
```
az group delete --name PubSubEvents --no-wait --yes
```
![](Evidences/Image15.png)


### [<-- Back to readme](../../readme.md)


