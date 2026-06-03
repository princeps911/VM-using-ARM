# Azure VM Deployment via ARM Template

## Deployment Commands
```powershell
# 1. Created a targeted resource group for open capacity
az group create --name rg-cloud-project-denmark --location denmarkeast

# 2. Executed template deployment with inline parameter location overrides
az deployment group create `
   --resource-group rg-cloud-project-denmark `
   --template-file azuredeploy.json `
   --parameters azuredeploy.parameters.json location=denmarkeast
## Verification Proof

### Successful Deployment Status
![Successful Deployment](screenshots/deployment-success.png)

### Proof of Connectivity (SSH Login)
![Proof of Connectivity](screenshots/proof-of-connectivity.png)
