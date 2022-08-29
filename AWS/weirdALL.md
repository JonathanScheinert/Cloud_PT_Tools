## A repository of useful functions (offensive & defensive) to interact with AWS services. 

weirdALL - https://github.com/carnal0wnage/weirdAAL/wiki

weirdALL is a complete auditing framework focusing on AWS services, configurations, user, roles, permissions and so on.

**Prerequisites** 
* Python requirements installed.
* weirdALL uses boto3 and it handles standard AWS keypair setups, copy env.sample to .env in your local file system and put in a AWS keypair.
* weirdALL uses a sqlite3 to store some data. This isn't optional. If you don't do this...Things. Will. Break.
  * $ python3 create_dbs.py

**Key features**
* Reacon module - Assuming the key works, the recon module will attempt to enumerate each service available to the boto3 v1.7.4 library. 
* You can list services by keys on the desired target.
  * Use available services to pivot for more data. For example: 
    * $ python3 weirdAAL.py -m list_services_by_key -t <myTarget>
    * $ python3 weirdAAL.py -m s3_list_buckets -t <myTarget>

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/wierdALL_1.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/wierdALL_2.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/wierdALL_3.png)
