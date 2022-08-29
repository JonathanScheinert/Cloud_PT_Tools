
## Pacu is an open-source AWS exploitation framework, designed for offensive security testing against cloud environments.

Pacu - https://github.com/RhinoSecurityLabs/pacu

Created and maintained by Rhino Security Labs, Pacu allows penetration testers to exploit configuration flaws within an AWS account, using modules to easily expand its functionality.

**Prerequisites** 
* Requires python version >=3.6
  * $ pip3 install -U pip
  * $ pip3 install -U pacu

**Key features**
* Similarly, to Metasploit, Pacu uses modules. To list them all in a sorted way, based on its purpose, just type ls command.
* Enumerate your permissions using the following command:
  * > run iam__enum_permissions
* enumerate permissions for all users, then simply run the command: 
  * > run iam__enum_permission --all-users
* Reconnaissance regarding EC2 service:
  * > run ec2__enum
* In order to have constant access to retrieved data without a need to scroll your terminal window or saving the output in the external files, this information is hidden behind the command:
  * > data <service name>
* In the exploit section of Pacu’s modules you will find pretty handy scripts, as updating user data on EC2 instances and get a reverse shell to your host and more.
* Offers persistent techniques
* Hide your actions from any monitoring service (like CloudTrail, CloudWatch alarms or GuardDuty) which may alarm administrators and block your further lateral movements. Run one command to enumerate all those monitoring services: 
  * > run detection__enum_services

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/Pacu_1.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/Pacu_2.png)
