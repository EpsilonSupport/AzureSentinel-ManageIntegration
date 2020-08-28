# Manage-Integration

This playbook will automatically attach alert evidence from Azure Sentinel alerts and send them to Connectwise Manage API to create a ticket.


Author: Ryan Goodling (based off playbook created by Yaniv Shasha - https://github.com/Azure/Azure-Sentinel/tree/master/Playbooks/Get-SentinelAlertsEvidence)

Deploy the solution
1. Go to the Playbook GitHub page.<br>
2. Press the "deploy to azure" button.<br>
3. Fill in this information:<br>
- Azure Sentinel Playbook Name<br>
- Azure Account with permissions to Sentinel Workspace<br>
- Azure Sentinel Workspace Name<br>
- Azure Sentinel Workspace resource group name<br>
- Number of events to pull from Azure Sentinel (default value is 10 latest events )<br>
- API User Name to connect to Connectwise Manage SIEM service board (in Last Pass)<br>
- API Private Key to connect to Connectwise Manage SIEM service board (in Last Pass)<br>
- API URI to connect to Connectwise Manage SIEM service board (in Last Pass)<br>
- API Developer ClientID to connect to Connectwise Manage SIEM service board (in Last Pass)<br>
- Company ID in Manage of client that you are configuring (Go to Manage - Companies - search for company - locate Company_RecID - may have to add column<br>

4.	Once the playbook is deployed, Go to playbook - Logic App Designer - expand any nodes with warnings and select account - and then connect.<br>
5.	Next, go to Configuration - Analytics and configure required alerts to use playbook. Edit Alert - Automated Response - Select Playbook.<br>
6.  Enable playbook once everything is set up correctly.

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FEpsilonSupport%2FAzureSentinel-ManageIntegration%2Fmaster%2FAzureDeploy-ManageIntegration.json)
