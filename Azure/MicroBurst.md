
## MicroBurst includes functions and scripts that support Azure Services discovery, weak configuration auditing, and post exploitation actions such as credential dumping. It is intended to be used during penetration tests where Azure is in use.

MicroBurst - https://github.com/NetSPI/MicroBurst

**Prerequisites** 
* Required Dependencies: Az, Azure, AzureRM, AzureAD, and MSOnline PowerShell Modules are all used in different scripts.
* Dependencies Note: Originally written with the AzureRM PS modules, older scripts have been ported to their newer Az equivalents

**Key features**
* Vault access is controlled by the Access Policies in each vault, but any users with Contributor rights are able to 	give themselves access to a Key Vault. Get-AzPasswords will not modify any Key Vault Access Policies, but you could give your account read permissions on the vault if you really needed to read a key.
* At the core of the script, we’re doing DNS lookups for blob.core.windows.net subdomains to enumerate valid storage accounts and then brute-force container names using the Azure Blob Service REST APIs.

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/MicroBurst_1.png)
