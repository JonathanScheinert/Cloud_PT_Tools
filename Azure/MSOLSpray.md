## A password spraying tool for Microsoft Online accounts (Azure/O365). 

MSOLSpray - https://github.com/dafthack/MSOLSpray

The script logs if a user cred is valid, if MFA is enabled on the account, if a tenant doesn't exist, if a user doesn't exist, if the account is locked, or if the account is disabled.

**Prerequisites** 
* You will need a user list file with target email addresses one per line. Open a PowerShell terminal from the Windows command line with 'powershell.exe -exec bypass'.

**Key features**
* Operates as a Microsoft Online recon tool that will provide account/domain enumeration. In limited testing it appears that on valid login to the Microsoft Online OAuth2 endpoint it isn't auto-triggering MFA texts/push notifications making this really useful for finding valid creds without alerting the target.
* The main difference with this tool to other password spraying which it is looking for valid passwords, but also the extremely verbose information Azure AD error codes give you. These error codes provide information relating to if MFA is enabled on the account, if a tenant doesn't exist, if a user doesn't exist, if the account is locked, if the account is disabled, if the password is expired and much more.


![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/MSOLSpray_1.png)


