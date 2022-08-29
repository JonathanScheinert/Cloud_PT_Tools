
## Collection of resources related to security benchmark frameworks. 

aws-security-benchmark - https://github.com/amazon-archives/aws-security-benchmark

Currently covered frameworks: Script to evaluate your AWS account against the full CIS Amazon Web Services Foundations Benchmark 1.1
The script has a number of different outputs, all optional by changing the settings inside the script.

**Prerequisites** 
* Requires python version >=3.6
* AWS key and secret configured through ~/.aws/credentials
* The IAM policy required to run the script is located in the file aws-cis-foundation-benchmark-checklist-lambdarole.json

**Key features**
* All outputs will generate a single report of all supported controls in short format, full JSON or HTML.
* Delivery of the report is console output for JSON structure, S3 SignedURL for HTML file and optional publish to SNS for the S3 SignedURL if you wish to receive an email or trigger other functions any time a new report is done, you can also store the reports in a central S3 bucket if you run this for multiple accounts.
* You can also run this script from an admin console using python and AWS SDK. It will use the credentials you have stored in your profiles.


![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/aws-security-benchmark_1.png)

