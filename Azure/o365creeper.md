## This is a simple Python script used to validate email accounts that belong to Office 365 tenants. 

o365creeper - https://github.com/LMGsec/o365creeper

This script takes either a single email address or a list of email addresses as input, sends a request to Office 365 without a password, and looks for the "IfExistsResult" parameter to be set to 0 for a valid account. Invalid accounts will return a 1.

**Prerequisites** 
* This script depends on the Python "Requests" library. 
* MSOnline PowerShell module installed.

**Key features**
* An easy-to-use email validator for Outlook mailboxes.
* The script can take a single email address with the -e parameter or a list of email addresses, one per line, with the -f parameter. 
* Additionally, the script can output valid email addresses to a file with the -o parameter.

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/o365creeper_1.png)

