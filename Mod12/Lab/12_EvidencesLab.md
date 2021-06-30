# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 12: Monitoring services that are deployed to Azure
In this lab we will learn how to create an Application Insights resource and integrate Application Insights telemetry tracking into an ASP.NET web application and a resource created with Azure App Service Web Apps.

### [Go to lab instructions -->](Files/AZ-204_12_lab.md)

## Working Architecture
![architecture12](architecture_12.png)

Create an Application Insights resource.
![](Evidences/Image1.png)


Create a web app by using Azure App Services resource.
![](Evidences/Image2.png)


Configure web app autoscale options.
![](Evidences/Image3.png)


Save configuration options.
![](Evidences/Image4.png)


Enter the following command to create a new .NET Web API application named SimpleApi in the current directory:
```
dotnet new webapi --output . --name SimpleApi
```
![](Evidences/Image5.png)


Enter the following command to import Microsoft.ApplicationInsights from NuGet to the current project:
```
dotnet add package Microsoft.ApplicationInsights
```
![](Evidences/Image6.png)


Enter the following command to import Microsoft.ApplicationInsights.AspNetCore from NuGet:
```
dotnet add package Microsoft.ApplicationInsights.AspNetCore
```
![](Evidences/Image7.png)


Enter the following command to import Microsoft.ApplicationInsights.PerfCounterCollector from NuGet to the current project:
```
dotnet add package Microsoft.ApplicationInsights.PerfCounterCollector
```
![](Evidences/Image8.png)


Enter the following command to build the .NET web app:
```
dotnet build
```
![](Evidences/Image9.png)


Update Startup class and enter the following command to build the .NET web app:
```
dotnet build
```
![](Evidences/Image10.png)


First enter the following command to run the .NET web application.
```
dotnet run
```
After go to the /weatherforecast relative path of your test application that's hosted at localhost on port 5000.
![](Evidences/Image11.png)


Get metrics in Application Insights.
![](Evidences/Image12.png)


Enter the following command to list all the apps in your MonitoredAssets resource group:
```
az webapp list --resource-group MonitoredAssets
```
![](Evidences/Image13.png)


Enter the following command to deploy the api.zip file to the web app:
```
az webapp deployment source config-zip --resource-group MonitoredAssets --src api.zip --name smpapiaas
```
![](Evidences/Image14.png)


In the browser address bar, update the URL by appending the suffix /weatherforecast to the end of the current URL.
![](Evidences/Image15.png)


Configure in-depth metric collection for Web Apps.
![](Evidences/Image16.png)


Get updated metrics in Application Insights.
![](Evidences/Image17.png)


View real-time metrics in Application Insights.
![](Evidences/Image18.png)


Enter the following command to delete the MonitoredAssets resource group:
```
az group delete --name MonitoredAssets --no-wait --yes
```
![](Evidences/Image19.png)


### [<-- Back to readme](../../readme.md)


