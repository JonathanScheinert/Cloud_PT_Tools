## Discover the most privileged entities in the target AWS environments - including the stealthy AWS Shadow Admins.

AWStealth - https://github.com/cyberark/SkyArk/tree/master/AWStealth

With the AWStealth’s scanning results - blue and red teamers can discover who are the users with the most sensitive and risky permissions.
Potential attackers are hunting for those users and the defensive teams must make sure these privileged users are well secured - have strong, rotated and safety stored credentials, have MFA enabled, being monitored carefully, etc.

**Prerequisites** 
* Download - AWS Tools for PowerShell
* Import-Module .\AWStealth.ps1 -force
* Open PowerShell in SkyArk folder with running scripts permission:
  * "powershell -ExecutionPolicy Bypass -NoProfile"
* Permissions for AWStealth – Read-only The built in "SecurityAudit" Job function.
	Or Read-Only permissions over the IAM

**Key features**
* The tool scan for the most privileged users in the AWS environment, display their roles and shows misconfigurations.
* When the scan is done, the tool creates a report in a CSV & Text formats for the testers to analyze.

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/AWSStealth_1.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/AWSStealth_2.png)
