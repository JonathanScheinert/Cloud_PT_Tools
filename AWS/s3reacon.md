## Amazon S3 bucket finder and crawler.

s3reacon - https://github.com/clarketm/s3recon

With the AzureStealth’s scanning results - blue and red teamers can discover who are the users with the most sensitive and risky permissions.
Potential attackers are hunting for those users and the defensive teams must make sure these privileged users are well secured - have strong, rotated and safety stored credentials, have MFA enabled, being monitored carefully, etc.

**Prerequisites** 
* s3recon requires python version >=3.6
* Download a wordlist.

**Key features**
* Expose public and private s3 buckets in the regions that were preconfigured in the s3recon.yml
* Brute-force s3 buckets using customized wordlists.

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/s3reacon_1.png)

