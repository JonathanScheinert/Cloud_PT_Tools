
## BlobHunter helps you identify Azure blob storage containers which store files that are publicly available to anyone with an internet connection.

Blob Hunter - https://github.com/cyberark/BlobHunter

The tool will help mitigate risk by identifying poorly configured containers that store sensitive data, which is specifically helpful in larger scale Azure subscriptions where there are a significant number of storage accounts that could be hard to track.

**Prerequisites** 
* Python 3.5+
* Azure CLI
* Azure user with one of the following built-in roles:
  * Owner
  * Contributor
  * Storage Account Contributor

**Key features**
* Scans the azure environment for publicly open blobs, efficient in disclosing information.



![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/BlobHunter_1.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/BlobHunter_2.png)
