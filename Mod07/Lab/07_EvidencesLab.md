# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 07: Access resource secrets more securely across services
In this lab we will learn how to create an Azure key vault and store secrets in the key vault, create a system-assigned managed identity for an Azure App Service instance, create a Key Vault access policy for an identity or application from Azure Active Directory and use the Azure SDK for .NET to download a blob with an Azure role.

### [Go to lab instructions -->](Files/AZ-204_07_lab.md)

## Working Architecture
![architecture07](architecture_07.png)

Create a storage account.
![](Evidences/Image1.png)


Create a key vault.
![](Evidences/Image2.png)


Create a functions app.
![](Evidences/Image3.png)


Configure a system-assigned managed service identity.
![](Evidences/Image4.png)


Create a Key Vault secret.
![](Evidences/Image5.png)


Configure a Key Vault access policy.
![](Evidences/Image6.png)


Configure a Key Vault access policy.
![](Evidences/Image7.png)


Key Vault access policy created successfully.
![](Evidences/Image8.png)


Create a Key Vault-derived application setting.
![](Evidences/Image9.png)


Enter the following command to use the Azure Functions Core Tools to create a new local Functions project in the current directory using the dotnet runtime:
```
func init --worker-runtime dotnet --force
```

Enter the following command to build the .NET Core project:
 ```
dotnet build
```
![](Evidences/Image10.png)


Enter the following command to create a new function named FileParser using the HTTP trigger template:
```
func new --template "HTTP trigger" --name "FileParser"
```
![](Evidences/Image11.png)


After update the FileParser class, enter the following command to run the function app project:
```
func start --build
```
We see that the function executes correctly.
![](Evidences/Image12.png)


Enter the following command to start the httprepl tool setting the base Uniform Resource Identifier (URI) to ``http://localhost:7071``:
```
httprepl http://localhost:7071
```
![](Evidences/Image13.png)


Enter the following command to publish the function app project:
```
func azure functionapp publish securefuncaas
```
![](Evidences/Image14.png)


Test the Key Vault-derived application setting.
![](Evidences/Image15.png)


Correct answer.
![](Evidences/Image16.png)


Create storage account containers.
![](Evidences/Image17.png)


Upload a blob into a container.
![](Evidences/Image18.png)


The JavaScript Object Notation (JSON) contents of the blob should now display.
![](Evidences/Image19.png)


Change access level policy to private.
![](Evidences/Image20.png)


An error message indicating that the resource wasn't found should now display.
![](Evidences/Image21.png)


Enter the following command to add Azure.Storage.Blobs package from NuGet:
```
dotnet add package Azure.Storage.Blobs
```
![](Evidences/Image22.png)


Update the FileParser class to write Azure Blob storage code using the Azure SDK for .NET.
Enter the following command to publish the function app project:
```
func azure functionapp publish securefuncaas
```
![](Evidences/Image23.png)


Test the function app.
![](Evidences/Image24.png)


Enter the following command to delete the ConfidentialStack resource group:
```
az group delete --name ConfidentialStack --no-wait --yes
```
![](Evidences/Image25.png)


### [<-- Back to readme](../../readme.md)


