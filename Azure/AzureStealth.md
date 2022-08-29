
## Discover the most privileged users in the target Azure environments - including the stealthy Azure Shadow Admins.

SkyArk - https://github.com/cyberark/SkyArk/tree/master/AzureStealth

With the AzureStealth’s scanning results - blue and red teamers can discover who are the users with the most sensitive and risky permissions.
Potential attackers are hunting for those users and the defensive teams must make sure these privileged users are well secured - have strong, rotated and safety stored credentials, have MFA enabled, being monitored carefully, etc.

**Prerequisites** 
* Az & AzureAD PowerShell modules
* Open PowerShell in the AzureStealth folder with the permission to run scripts:
  * powershell -ExecutionPolicy Bypass -NoProfile"
  * Import-Module .\AzureStealth.ps1 -Force
* AzureStealth only needs Read-Only permissions over the Azure Directory and Subscriptions that you wish to scan.

**Key features**
* The tool scan for the most privileged users in the Azure environment, display their roles and shows misconfigurations.
* When the scan is done, the tool creates a report in a CSV & Text formats for the testers to analyze. 
* Running AzureStealth is also available using PowerShell \ Cloud Shell - you can load and run the scan directly from GitHub, simply use the following commands:
  * (1) IEX (New-Object Net.WebClient).DownloadString('https://raw.githubusercontent.com/cyberark/SkyArk/master/AzureStealth/AzureStealth.ps1')  
  * (2) Scan-AzureAdmins  



![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/AzureStealth_1.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/AzureStealth_2.png)
