
## Cloudtracker helps you find over-privileged IAM users and roles by comparing CloudTrail logs with current IAM policies.

cloudtracker - https://github.com/duo-labs/cloudtracker

Intro post: https://duo.com/blog/introducing-cloudtracker-an-aws-cloudtrail-log-analyzer
This document will describe the setup that uses Athena and how to use the tool. Cloudtracker no longer requires Elasticsearch, but if you'd like to use Cloudtracker with Elasticsearch please see Elasticsearch installation and ingestion.

**Prerequisites** 
* Download a copy of the IAM data of an account using the AWS CLI:
  * $ mkdir -p account-data
  * $ aws iam get-account-authorization-details > account-data/demo_iam.json
* Create a config.yaml file with contents similar to:
  * Athena:
		  s3_bucket: <my_log_bucket>
		  path: <my_prefix>
		accounts:
		  - name: <account-name>
		    id: 111111111111
		    iam: account-data/demo_iam.json
  * You will need the privilege arn:aws:iam::aws:policy/AmazonAthenaFullAccess and also s3:GetObject and s3:ListBucket for the S3 bucket containing the CloudTrail logs.


**Key features**
•	This will perform all of the initial setup which takes about a minute. Subsequent calls will be faster:
o	$ cloudtracker --account <account-name> --list users
•	Note that not all AWS activities are stored in CloudTrail logs. Specifically, data level events such as reading and writing S3 objects, putting CloudWatch metrics, and more.
* List account roles as follows:
  * $ cloudtracker --account <account-name> --list roles --start 2018-01-01
* Listing actions of actors: The main purpose of Cloudtracker is to look at the API calls made by actors (users and roles).
  * $ cloudtracker --account <account-name> --user <any-user>
* As there may be a lot of unused or unknown actions, we can filter things down:
  * $ cloudtracker --account <account-name> --user <any-user> --show-used
* Output explanation - CloudTracker shows a diff of the privileges granted vs used. The symbols mean the following:
  * No symbol means this privilege is used, so leave it as is.
  * - A minus sign means the privilege was granted, but not used, so you should remove it.
  * ? A question mark means the privilege was granted, but it is unknown if it was used because it is not recorded in CloudTrail.
  * + A plus sign means the privilege was not granted, but was used. The only way this is possible is if the privilege was previously granted, used, and then removed, so you may want to add that privilege back.


![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/CloudTracker_!.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/CloudTracker_2.png)
