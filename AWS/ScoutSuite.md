## Scout Suite is an open-source multi-cloud security-auditing tool, which enables security posture assessment of cloud environments. 

ScoutSuite - https://github.com/nccgroup/ScoutSuite

Using the APIs exposed by cloud providers, Scout Suite gathers configuration data for manual inspection and highlights risk areas. Rather than going through dozens of pages on the web consoles, Scout Suite presents a clear view of the attack surface automatically.

**Prerequisites** 
* AWS access key ID & secret access key / GCP user account creds / Azure user account creds:
* Amazon Web Services
  * $ python scout.py aws
* Azure
  * $ python scout.py azure --cli
* Google Cloud Platform
  * $ python scout.py gcp --user-account
* The following AWS Managed Policies can be attached to the principal used to run Scout in order to grant the necessary permissions:
  * ReadOnlyAccess
  * SecurityAudit
* Python installation requirements.

**Key features**
* Performs AWS API calls to fetch configuration data and identify security gaps, it is not necessary to complete and submit the AWS Vulnerability / Penetration Testing Request Form.
* Being able to export the tool's finding into arbitrary format that may be consumed by other tools or used to populate internal tracking system.
* One tool - all configuration checks in one place for speed and simplicity.
* Persistent monitoring - so you know about changes or issues as they arise.
* Generates an attack surface report.

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/ScoutSuite_1.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/ScoutSuite_2.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/ScoutSuite_3.png)
