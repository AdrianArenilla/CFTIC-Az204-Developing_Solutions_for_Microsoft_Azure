# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 08: Creating a multi-tier solution by using services in Azure
In this lab we will learn how to create a web application from a Docker Hub container image, create an API Management account, and configure an API as a proxy for another Azure service with header and payload manipulation.

### [Go to lab instructions -->](Files/AZ-204_08_lab.md)

## Working Architecture
![architecture08](architecture_08.png)

Create a web app.
![](Evidences/Image1.png)


Test the httpbin web application.
![](Evidences/Image2.png)


Test the httpbin web application.
![](Evidences/Image3.png)


Test the httpbin web application.
![](Evidences/Image4.png)


Create an API Management resource.
![](Evidences/Image5.png)


Define a new API.
![](Evidences/Image6.png)


Define a new API.
![](Evidences/Image7.png)


Add operation to a new API.
![](Evidences/Image8.png)


Add policy to a new API.
![](Evidences/Image9.png)


Add request to a new API.
![](Evidences/Image10.png)


Test the API.
![](Evidences/Image11.png)


Observe the HTTP response.
![](Evidences/Image12.png)


Results created previously.
![](Evidences/Image13.png)


Manipulate an API response.
![](Evidences/Image14.png)


Test the API response.
![](Evidences/Image15.png)


Observe the HTTP response.
![](Evidences/Image16.png)


Replace that block of XML with the following XML:
```
<outbound>
     <base />
     <xml-to-json kind="direct" apply="always" consider-accept-header="false" />
</outbound>
```
![](Evidences/Image17.png)


The new results are in JavaScript Object Notation (JSON) format.
![](Evidences/Image18.png)


The new results are in JavaScript Object Notation (JSON) format.
![](Evidences/Image19.png)


The new results are in JavaScript Object Notation (JSON) format.
![](Evidences/Image20.png)


Enter the following command to delete the ApiService resource group:
```
az group delete --name ApiService --no-wait --yes
```
![](Evidences/Image21.png)


### [<-- Back to readme](../../../../)


