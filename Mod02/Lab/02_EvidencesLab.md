# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 02: Implement task processing logic by using Azure Functions
In this lab we will learn how to create an Azure Functions application, create a local Azure Functions project with its core tools and create multiple functions using built-in triggers and input integrations.

### [Go to lab instructions -->](Files/AZ-204_02_lab.md)

## Working Architecture
![architecture02](architecture_02.png)

Create a storage account.
![](Evidences/Image1.png)


Storage account created.
![](Evidences/Image2.png)


Function app in marketplace.
![](Evidences/Image3.png)


Create function app.
![](Evidences/Image4.png)


Function app created.
![](Evidences/Image5.png)


Enter the following command to use the Azure Functions Core Tools to create a new local Azure Functions project in the current directory using the dotnet runtime:
```
func init --worker-runtime dotnet --force
```
![](Evidences/Image6.png)


Update the value of the AzureWebJobsStorage by setting it to the connection string.
![](Evidences/Image7.png)


Enter the following command to build the project:
 ```
 dotnet build
 ```
![](Evidences/Image8.png)


Enter the following command to use the Azure Functions Core Tools to create a new function named Echo using the HTTP trigger template:
```
func new --template "HTTP trigger" --name "Echo"
```
![](Evidences/Image9.png)


Update the content of the Echo.cs file.
![](Evidences/Image10.png)


Enter the following command to run the function app project:
```
func start --build
```
![](Evidences/Image11.png)


Enter the following command to start the httprepl tool setting the base Uniform Resource Identifier (URI) to ``http://localhost:7071``:
```
httprepl http://localhost:7071
```
![](Evidences/Image12.png)


Enter the following command to run the post command that sends an HTTP request body set to a numeric value or a text string using the \ - \ - content option:

```
post --content 3
```
```
post --content 5
```
```
post --content "Hello"
```
```
post --content "{"msg": "Successful"}"
```
![](Evidences/Image13.png)


Post and body of the file when executing the template.
![](Evidences/Image14.png)


Request received correctly.
![](Evidences/Image15.png)


Enter the following command to use the Azure Functions Core Tools to create a new function named Recurring using the Timer trigger template:
```
func new --template "Timer trigger" --name "Recurring"
```
![](Evidences/Image16.png)


Enter the following command to run the function app project:
```
func start --build
```
![](Evidences/Image17.png)


Update the content of the Recurring.cs file.
![](Evidences/Image18.png)


Enter the following command to run the function app project:
```
func start --build
```
![](Evidences/Image19.png)


Upload sample content to Azure Blob Storage.
![](Evidences/Image20.png)


Enter the following command to use the Azure Functions Core Tools to create a new function named GetSettingInfo using the HTTP trigger template:
```
func new --template "HTTP trigger" --name "GetSettingInfo"
```
![](Evidences/Image21.png)


After updating the GetSettingInfo.cs file install the Nuget "Storage" extension.
```
func extensions install --package Microsoft.Azure.WebJobs.Extensions.Storage
```
![](Evidences/Image22.png)


Correct compilation.
![](Evidences/Image23.png)


Enter the following command to validate the extensions were installed correctly by building the .NET project:
```
dotnet build
```
![](Evidences/Image24.png)


First enter the following command to run the function app project:
```
func start --build
```
After enter the following command to start the httprepl tool setting the base Uniform Resource Identifier (URI) to ``http://localhost:7071``:
```
httprepl http://localhost:7071
```
![](Evidences/Image25.png)


Enter the following command to publish the function app project:
```
func azure functionapp publish funclogicaas
```
![](Evidences/Image26.png)


Validate deployment.
![](Evidences/Image27.png)


The results of the test run in JSON format.
![](Evidences/Image28.png)


Enter the following command to delete the Serverless resource group:
```
az group delete --name Serverless --no-wait --yes
```
![](Evidences/Image29.png)


### [<-- Back to readme](../../../../)