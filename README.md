[![Build status](https://ci.appveyor.com/api/projects/status/ch4ph3xdg4i44a98/branch/master?svg=true)](https://ci.appveyor.com/project/olandese/bigdataingestion1/branch/master)

# BigDataIngestion Part 1

## Option 1: Deploy directly from the portal

1. Click this button (hold CTRL while clicking to open in a new tab):

    <a target="_blank" id="deploy-to-azure"  href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FDutchAzureMeetup%2FBigDataIngestion1%2Fmaster%2Fsrc%2FAzureInfrastructure%2Fazuredeploy.json"><img src="http://azuredeploy.net/deploybutton.png"/></a>

2. Fill the required settings
3. Start the Stream Analytics Job

## Option 2: Deploy Azure Resources from PowerShell 

Please follow this steps to get everything working: 

1. Clone this repo: https://github.com/DutchAzureMeetup/BigDataIngestion1.git
2. In your favorite text editor open this file: \src\AzureInfrastructure\azuredeploy.parameters.json
3. Change the value of the "projectName" to something else and save the file (projectName must be between 3 and 20 characters in length and use numbers and lower-case letters only).
4. In a powershell prompt navigate to this directory: \src\AzureInfrastructure
5. Login in azure with your credentials: **Login-AzureRmAccount**
6. **[Optional]** Follow this only if you have multiple Azure subscriptions:

  6.1 Get a list of your subscriptions: **Get-AzureRmSubscription**  
  6.2 Select the subscription which you want to use: **Select-AzureRmSubscription -SubscriptionId** {put here your subscriptionid}
  
7. Deploy: **.\deploy.ps1**
8. Start the Stream Analytics Job
