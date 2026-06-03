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