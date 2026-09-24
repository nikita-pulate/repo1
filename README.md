## Get to know about Azure 
- What is Azure?
- https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-azure
  <img width="1600" height="573" alt="WhatsApp Image 2026-08-24 at 10 48 28 PM" src="https://github.com/user-attachments/assets/83c11744-6bde-449f-b61a-7aab19ed192c" />



<img width="1522" height="1170" alt="WhatsApp Image 2026-08-24 at 10 48 30 PM" src="https://github.com/user-attachments/assets/030a9ec1-cb15-4005-b751-fb2971fad3ff" />




## Providing cloud service models
- **Infrastructure as a service (IaaS)** delivers essential IT infrastructure for businesses to flexibly create and manage resources.
- **Platform as a service (PaaS)** offers a cloud platform to develop, run, and manage applications without the need to handle underlying infrastructure.
- **Software as a service (SaaS)** provides seamless access to software applications over the internet, eliminating local installation needs.
- **Artificial intelligence as a service (AIaaS)** provides AI tools and services via the cloud to accelerate innovation.
- **Model as a service (MaaS)** delivers machine learning models as serverless APIs for simplified app deployment.

## Azure Portal walkthrough
<img width="1470" height="825" alt="WhatsApp Image 2026-09-24 at 12 25 46 PM" src="https://github.com/user-attachments/assets/69da1733-2ea9-45fe-a182-78d93ee3c4f4" />

<img width="1600" height="939" alt="WhatsApp Image 2026-09-24 at 12 25 50 PM" src="https://github.com/user-attachments/assets/21689dd7-e400-430b-97f5-bdd883980e56" />



<img width="1386" height="1060" alt="WhatsApp Image 2026-09-24 at 12 25 54 PM" src="https://github.com/user-attachments/assets/79d16e5d-b88b-457e-8d43-5fc2908a9327" />



## Active Azure Regions in India
- Central India (Pune): Located locally, features multi-availability zones, and serves as a primary production region.
- South India (Chennai): Acts as a primary disaster recovery and geo-redundant storage partner for other domestic regions.
- West India (Mumbai): Handles secondary deployments and network edge capabilities.
- South Central India (Hyderabad): Functions as an expanded high-capacity region geared towards modern cloud and AI workloads.



## Introduction to Azure Cloud Shell 

Azure Cloud Shell is an online-based shell provided by Microsoft Azure that allows users to manage their Azure resources directly from a web browser. It offers a pre-configured environment with popular command-line tools and programming languages, enabling users to execute scripts, manage resources, and automate tasks without the need for local installations.

## Launch VM using Azure Cloud Shell

### Step 1: Open Azure Cloud Shell
1. Go to the [Azure Portal](https://portal.azure.com).
2. Click on the Cloud Shell icon (>) in the top right corner.

### Step 2: Create a Resource Group
```bash
az group create   --name myResourceGroup   --location centralindia
```

### Step 3: Create a Virtual Machine
```bash
az vm create \
  --resource-group myResourceGroup \
  --name myVM \
  --image Ubuntu2204 \
  --size Standard_B2ats_v2 \
  --admin-username azureuser \
  --generate-ssh-keys
```
### Step 4: Verify the VM Creation
```bash
az vm show --resource-group myResourceGroup --name myVM --output table
```

### step 5: Connect to the Virtual Machine
```bash
ssh azureuser@<public-ip-address>
```
### Step 6: Clean Up Resources VM, resource group
```bash
az vm delete --resource-group myResourceGroup --name myVM --yes
az group delete --name myResourceGroup --yes --no-wait
```















  
