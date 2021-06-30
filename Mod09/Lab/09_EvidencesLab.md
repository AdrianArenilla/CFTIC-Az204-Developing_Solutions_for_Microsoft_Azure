# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab Logic Apps: Automate business processes with Logic Apps
In this lab we will learn how to create a workflow with the Logic App, manage products and APIs with the Logic App, and use Azure API Management as a proxy for the Logic App.

### [Go to lab instructions -->](Files/AZ-204_09_lab.md)

## Working Architecture
![architecture09](architecture_09.png)

Create an API Management.
![](Evidences/Image1.png)


Create a Logic App.
![](Evidences/Image2.png)


Create a storage account.
![](Evidences/Image3.png)


Upload sample content to Azure Files.
![](Evidences/Image4.png)


Upload files into a file share.
![](Evidences/Image5.png)


Create a trigger for the workflow.
![](Evidences/Image6.png)


Select Request into Logic Apps DesignerS.
![](Evidences/Image7.png)


In the When a HTTP request is received within the method, select GET.
![](Evidences/Image8.png)


Create an action to query Azure Storage file shares. 
In the List files area, in the Folder text box, enter /metadata.
![](Evidences/Image9.png)


Create an action to project list item properties.
![](Evidences/Image10.png)


Build an HTTP response action.
![](Evidences/Image11.png)


All workflow.
![](Evidences/Image12.png)


Create an API integrated with Logic Apps.
![](Evidences/Image13.png)


Create an API integrated with Logic Apps.
![](Evidences/Image14.png)


Test the API operation.
![](Evidences/Image15.png)


Test the API operation.
![](Evidences/Image16.png)


Enter the following command to delete the AutomatedWorkflow resource group:
```
az group delete --name AutomatedWorkflow --no-wait --yes
```
![](Evidences/Image17.png)


### [<-- Back to readme](../../../../)


