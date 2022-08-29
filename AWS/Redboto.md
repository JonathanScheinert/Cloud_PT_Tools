
## Redboto is a collection of scripts that use the Amazon SDK for Python boto3 to perform red team operations against the AWS API.

Redboto - https://github.com/ihamburglar/Redboto

With the AzureStealth’s scanning results - blue and red teamers can discover who are the users with the most sensitive and risky permissions.
Potential attackers are hunting for those users and the defensive teams must make sure these privileged users are well secured - have strong, rotated and safety stored credentials, have MFA enabled, being monitored carefully, etc.

**Prerequisites** 
* Install the pre-requisite libraries with:
  * $ pip install cryptography boto3 texttable


**Key features**
* Retrieves data regarding EC2 instances, searches for left behind keys and secrets, looks for startup scripts in EC2s and also able to run shell script on a remote machine.

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/Redboto_1.png)

