[![Deploy to Azure](https://azuredeploy.net/deploybutton.svg)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Factive-labs%2FAzureHashcat%2Fmaster%2Fazuredeploy.json) [![Visualize](http://armviz.io/visualizebutton.png)](http://armviz.io/#?load=https%3A%2F%2Fraw.githubusercontent.com%2Factive-labs%2FAzureHashcat%2Fmaster%2Fazuredeploy.json)

# Hashcat Azure

This is a template for setting up and deploying [hashcat](https://hashcat.net/) and [John the Ripper](https://www.openwall.com/john/) on Azure using NC-series virtual machines and GRID drivers. Click above button to deploy on [Microsoft Azure](https://azure.microsoft.com/) (requires an Azure subscription).

## Usage
Once deployed, connect to the server with SSH and use hashcat from the commandline. See the [Hashcat Wiki](https://hashcat.net/wiki/) for details and examples.

## How it works
The deployment will create an Ubuntu Server 20.04 LTS instance on an Azure NC-series virtual machine. The deployment process executes a custom script to [install NVIDIA GRID drivers](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/n-series-driver-setup#install-grid-drivers-on-nv-or-nvv2-series-vms) as well as the latest released version of hashcat.

## Notes
Forked from here https://github.com/carlmon/Hashcat-Azure