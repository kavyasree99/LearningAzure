## Create VM using Azure CLI

### Start with creating a Resource Group

```
az group create --name learn-cli --location westus
```

### Set the Resource Group as default (if required)

```
az config set defaults.group=learn-azure-cli
```

### Create VM with Vnet & Subnet

```
az vm create --resource-group learn-cli --name VMCLI --image Ubuntu2204 --vnet-name default --subnet default --generate-ssh-keys --output json --verbose
```

### Delete the Resource Group to delete all the resources

```
az group delete --name learn-cli
```
