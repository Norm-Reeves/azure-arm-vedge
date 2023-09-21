# azure-arm-vedge

Deployment template to deploy VMware SD-WAN By VeloCloud to Azure.

Mirrored source (https://github.com/vmwarecode/VMware-SD-WAN-By-VeloCloud-Azure-Resource-Manager-Template). Added readme to allow deployment directly from GitHub and to notate important information such as known issues and changes made. Fixed a nic3 dependency that would cause a failure in deployment.

Deploying
=========

1.) Open template link: https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FNorm-Reeves%2Fazure-arm-vedge%2F0.3%2FVMware%20SD-WAN%20By%20VeloCloud%20ARM%20Template%20(20191008).json

2.) Edit attributes as needed and deploy.

3.) Deployment will start, wait until the deployment goes to state "Succeeded".

4.) Confirm in TPX Network Orchestrator that the circuit is activated (may take 15 minutes).


Change Log:
============
0.0:

  • Mirrored source (https://github.com/vmwarecode/VMware-SD-WAN-By-VeloCloud-Azure-Resource-Manager-Template) and confirmed working.
  
0.1:

  • Added readme to allow deployment directly from GitHub and to notate important information such as known issues and changes made.

0.2:

  • Added dependency "[variables('networkSecurityGroupName')]" for nic3.

0.3:

  • Edited "Instance details" to our TPx/Azure environment.
  
  • Changed nic 1 & 2 to static assignment.

Known Issues & Desired Features:
============
1.) The resource group used needs to be the same as the VNET's.

2.) Handle variables in a parameters.json file.

3.) Get rid of nic1 which is not used to enable the use of more cost-effective VM sizes.
