# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 13: Enhancing a web application by using the Azure Content Delivery Network
In this lab, we will learn how to register a Microsoft.CDN resource provider, create content delivery network resources, and create and configure Content Delivery Network endpoints that are linked to multiple Azure services.

### [Go to lab instructions -->](Files/AZ-204_13_lab.md)

## Working Architecture
![architecture13](architecture_13.png)

Create a storage account.
![](Evidences/Image1.png)


Create a web app.
![](Evidences/Image2.png)


At the Cloud Shell command prompt in the portal, enter the following command to get the version of the Azure Command-Line Interface (Azure CLI) tool:
```
az --version
```
![](Evidences/Image3.png)


Observe the list of currently registered providers. The Microsoft.CDN provider is currently in the list of providers.
![](Evidences/Image4.png)


If the Microsoft.CDN provider is not listed, enter the following command:
```
az provider register --namespace Microsoft.CDN
```
![](Evidences/Image5.png)


Create a Content Delivery Network profile.
![](Evidences/Image6.png)


Configure Storage containers (media).
![](Evidences/Image7.png)


Configure Storage containers (video)
![](Evidences/Image8.png)


Storage containers created.
![](Evidences/Image9.png)


Create Content Delivery Network endpoints (media).
![](Evidences/Image10.png)


Create Content Delivery Network endpoints (video).
![](Evidences/Image11.png)


Create Content Delivery Network endpoints (web).
![](Evidences/Image12.png)


Observe the landing page.
![](Evidences/Image13.png)


Upload Storage blobs (media).
![](Evidences/Image14.png)


Upload Storage blobs (video).
![](Evidences/Image15.png)


Configure Web App settings (media).
![](Evidences/Image16.png)


Configure Web App settings (video).
![](Evidences/Image17.png)


Web App settings created and saved.
![](Evidences/Image18.png)


Validate the corrected landing page.
![](Evidences/Image19.png)


Test Content Delivery Network endpoints (media .jpg).
![](Evidences/Image20.png)


Test Content Delivery Network endpoints (media .jpg).
![](Evidences/Image21.png)


Test Content Delivery Network endpoints (media .jpg).
![](Evidences/Image22.png)


Test Content Delivery Network endpoints (video .mp4).
![](Evidences/Image23.png)


Update the Web App settings (media).
![](Evidences/Image24.png)


Update the Web App settings (video).
![](Evidences/Image25.png)


Restart the Web App.
![](Evidences/Image26.png)


Test the web content.
![](Evidences/Image27.png)


Enter the following command to delete the MarketingContent resource group:
```
az group delete --name MarketingContent --no-wait --yes
```
![](Evidences/Image28.png)


### [<-- Back to readme](../../../../)


