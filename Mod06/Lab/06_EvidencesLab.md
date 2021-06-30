# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 06: Authenticating to and querying Microsoft Graph by using MSAL and .NET SDKs
In this lab we will learn how to create a new application registry in Azure Active Directory (Azure AD), use the MSAL.NET library to implement the interactive authentication flow, obtain a token from the Microsoft identity platform using the MSAL.NET library and query the Microsoft Graph using the Microsoft Graph SDK and the device code flow.

### [Go to lab instructions -->](Files/AZ-204_06_lab.md)

## Working Architecture
![architecture06](architecture_06.png)

Create an Azure Active Directory (Azure AD) application registration.
![](Evidences/Image1.png)


Enable the default client type.
![](Evidences/Image2.png)


Enter the following command to create a new .NET project named GraphClient in the current folder:
```
dotnet new console --name GraphClient --output .
```
![](Evidences/Image3.png)


Enter the following command to import Microsoft.Identity.Client from NuGet:
```
dotnet add package Microsoft.Identity.Client
```
![](Evidences/Image4.png)


Enter the following command to build the .NET web application:
```
dotnet build
```
![](Evidences/Image5.png)


After update the Program class running the following command:
```
dotnet run
```
The browser window automatically opens the web page permissions requested.
![](Evidences/Image6.png)


We visualize the access token.
![](Evidences/Image7.png)


Enter the following command to import Microsoft.Graph from NuGet:
```
dotnet add package Microsoft.Graph
```
![](Evidences/Image8.png)


Enter the following command to import Microsoft.Graph.Auth from NuGet:
```
dotnet add package Microsoft.Graph.Auth
```
![](Evidences/Image9.png)


Enter the following command to build the .NET web application:
```
dotnet build
```
![](Evidences/Image10.png)


After update the Program class running the following command:
```
dotnet run
```
In an open browser window, go to https://microsoft.com/devicelogin.
and enter the code shown in the terminal.
![](Evidences/Image11.png)


Paste code.
![](Evidences/Image12.png)


Correct code.
![](Evidences/Image13.png)


Application successfully registered within Azure Active Directory.
![](Evidences/Image14.png)


Delete the application registration in Azure AD.
![](Evidences/Image15.png)


Delete the application registration in Azure AD.
![](Evidences/Image16.png)


### [<-- Back to readme](../../readme.md)


