# Lab 2: Manage Linux VMs with the Azure CLI

1. Create resource group
2. Create virtual machine
3. Connect to VM
4. Understand VM images
5. Understand VM sizes
6. VM power states
7. Management tasks

### Notes:

Quickstart: Create a Linux VM
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-vm

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart

Resurce group was created (Dayofirstassignmet)
connected to my VM 
az vm create \
    --resource-group DayofirstAssignment \
    --name DHoney \
    --image UbuntuLTS \
    --size Standard_F4s \
    --generate-ssh-keys
After connecting to VM
ssh -i .\Downloads\modeez.pem Dhoney@20.120.30.10

Tried to run it and got an Error message but was tried again and it when through
Starting and stopping my VM working using the command 
