# Microsoft Az-204 (Adrián Arenilla Seco)

## Lab 05: Deploying compute workloads by using images and containers
In this lab we will learn how to create a virtual machine using the Azure command line interface (CLI), deploy a Docker container image in Azure Container Registry and deploy a container from a container image in Container Registry using Container Instances.

### [Go to lab instructions -->](Files/AZ-204_05_lab.md)

## Working Architecture
![architecture05](architecture_05.png)

Create a resource group.
![](Evidences/Image1.png)


Enter the following command at the Cloud Shell to get the version of the Azure CLI tool:
```
az --version
```
![](Evidences/Image2.png)


Enter the following command to create a new virtual machine.
```
az vm create --resource-group ContainerCompute --name quickvm --image Debian --admin-username student --admin-password StudentPa55w.rd
```
![](Evidences/Image3.png)


Enter the following command to get a more detailed JavaScript Object Notation (JSON) file that contains various metadata about the newly created VM:
```
az vm show --resource-group ContainerCompute --name quickvm
```
![](Evidences/Image4.png)


Enter the following command to list all the IP addresses associated with the VM:
```
az vm list-ip-addresses --resource-group ContainerCompute --name quickvm
```
![](Evidences/Image5.png)


Enter the following command to filter the output to only return the first IP address value:
```
az vm list-ip-addresses --resource-group ContainerCompute --name quickvm --query '[].{ip:virtualMachine.network.publicIpAddresses[0].ipAddress}' --output tsv
```
![](Evidences/Image6.png)


Enter the following command to store the results of the previous command in a new Bash shell variable named ipAddress:
```
ipAddress=$(az vm list-ip-addresses --resource-group ContainerCompute --name quickvm --query '[].{ip:virtualMachine.network.publicIpAddresses[0].ipAddress}' --output tsv)
```

Enter the following command to render the value of the Bash shell variable ipAddress:
```
echo $ipAddress
```
![](Evidences/Image7.png)


Enter the following command to connect to the VM that you created earlier by using the Secure Shell (SSH) tool and the IP address stored in the Bash shell variable ipAddress:
```
ssh student@$ipAddress
```
![](Evidences/Image8.png)


Enter the following command to move from the root directory to the \~/clouddrive directory:
```
cd ~/clouddrive
```

Enter the following command to create a new directory named ipcheck in the \~/clouddrive directory:
```
mkdir ipcheck
```

Enter the following command to change the active directory from \~/clouddrive to \~/clouddrive/ipcheck:
```
cd ~/clouddrive/ipcheck
```

Enter the following command to create a new .NET console application in the current directory:
```
dotnet new console --output . --name ipcheck
```

Enter the following command to create a new file in the \~/clouddrive/ipcheck directory named Dockerfile:
```
touch Dockerfile
```

Enter the following command to open to open the embedded graphical editor in the context of the current directory:
```
code .
```
![](Evidences/Image9.png)


Update the Program class.
![](Evidences/Image10.png)


Enter the following command to run the application:
```
dotnet run
```
![](Evidences/Image11.png)


Update the Dockerfile file.
![](Evidences/Image12.png)


Create a Container Registry resource.
![](Evidences/Image13.png)


Enter the following command at the Cloud Shell to get a list of all container registries in your subscription:
```
az acr list
```
![](Evidences/Image14.png)


Enter the following command to view the container registry name:
```
az acr list --query "max_by([], &creationDate).name" --output tsv
```

Enter the following command to store the output of the above command in a new Bash shell variable called acrName.
```
acrName=$(az acr list --query "max_by([], &creationDate).name" --output tsv)
```

Enter the following command to render the value of the Bash shell variable acrName:
```
echo $acrName
```
![](Evidences/Image15.png)


Enter the following command to change the active directory from \~/ to \~/clouddrive/ipcheck:
```
cd ~/clouddrive/ipcheck
```

Enter the following command to get the contents of the current directory:
```
dir
```

Enter the following command to upload the source code to your container registry and build the container image as a Container Registry task:
```
az acr build --registry $acrName --image ipcheck:latest .
```
![](Evidences/Image16.png)


Create a container instance to enable the admin user in Container Registry.
![](Evidences/Image17.png)


Automatically deploy a container image to an Azure container instance.
![](Evidences/Image18.png)


Manually deploy a container image to Container Instances.
![](Evidences/Image19.png)


Validate that the container instance ran successfully.
![](Evidences/Image20.png)


Validate that the container instance ran successfully.
![](Evidences/Image21.png)


Enter the following command to delete the ContainerCompute resource group:
```
az group delete --name ContainerCompute --no-wait --yes
```
![](Evidences/Image22.png)


### [<-- Back to readme](../../../../)


