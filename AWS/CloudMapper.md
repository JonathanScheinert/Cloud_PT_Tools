## Cloudmapper helps you analyze your Amazon Web Services (AWS) environments. 

Cloudmapper - https://github.com/duo-labs/cloudmapper

The original purpose was to generate network diagrams and display them in your browser (functionality no longer maintained). It now contains much more functionality, including auditing for security issues.

**Prerequisites** 
* Requires python version >=3.6
* You will also need jq (https://stedolan.github.io/jq/) and the library pyjq (https://github.com/doloopwhile/pyjq), which require some additional tools installed.
* Copy the config.json.demo to config.json and edit it to include your account ID and name (ex. "prod"), along with any external CIDR names. A CIDR is an IP range such as 1.2.3.4/32 which means only the IP 1.2.3.4.
* You must have AWS credentials configured that can be used by the CLI with read permissions for the different metadata to collect.
* You must have the following privileges (these grant various read access of metadata):
   * - arn:aws:iam::aws:policy/SecurityAudit
   * - arn:aws:iam::aws:policy/job-function/ViewOnlyAccess

**Key features**
* Collecting the data is done as follows:
  * $ python cloudmapper.py collect --account <my_account>
* Analyzing the data is done as follows: 
   * $ python cloudmapper.py report --account <my_account>
   * $ python cloudmapper.py webserver
   * Then view the report in your browser at 127.0.0.1:8000/account-data/report.html
* If you use AWS Organizations, you can also automatically add organization member accounts to config.json using:
  * You need to be authenticated to the AWS CLI and have the permission - organization:ListAccounts prior to running this command.
    * $ python cloudmapper.py configure discover-organization-accounts
* Running Cloudmapper regularly to audit your environment is done as follows:
  * $ python cloudmapper.py audit --account <my_account>

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/CloudMapper_1.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/CloudMapper_2.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/CloudMapper_3.png)
