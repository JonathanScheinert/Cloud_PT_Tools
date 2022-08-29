## A script to enumerate Google Storage buckets, determine what access you have to them, and determine if they can be privilege escalated.

GCPBucketBrute - https://github.com/RhinoSecurityLabs/GCPBucketBrute

With the AzureStealth’s scanning results - blue and red teamers can discover who are the users with the most sensitive and risky permissions.
Potential attackers are hunting for those users and the defensive teams must make sure these privileged users are well secured - have strong, rotated and safety stored credentials, have MFA enabled, being monitored carefully, etc.

**Prerequisites** 
* Linux/OS X, Windows only works for unauthenticated scans. Something is wrong with how the script uses the subprocess module in that it fails when using an authenticated Google client.
  * Python3
  * Pip3

**Key features**
* This script (optionally) accepts GCP user/service account credentials and a keyword.
* Then, a list of permutations will be generated from that keyword which will then be used to scan for the existence of Google Storage buckets with those names.
* If credentials are supplied, the majority of enumeration will still be performed while unauthenticated, but for any bucket that is discovered via unauthenticated enumeration, it will attempt to enumerate the bucket permissions using the TestIamPermissions API with the supplied credentials. This will help find buckets that are accessible while authenticated, but not while unauthenticated.
* Regardless if credentials are supplied or not, the script will then try to enumerate the bucket permissions using the TestIamPermissions API while unauthenticated. This means that if you don't enter credentials, you will only be shown the privileges an unauthenticated user has, but if you do enter credentials, you will see what access authenticated users have compared to unauthenticated users.
* WARNING: If credentials are supplied, your username can be disclosed in the access logs of any buckets you discover.

![Import Module](./Screenshots/GCPBukcetBrute_1.png)
