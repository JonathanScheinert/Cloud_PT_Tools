
## Find interesting Amazon S3 Buckets by watching certificate transparency logs. 

BucketStream - https://github.com/eth0izzle/bucket-stream

This tool simply listens to various certificate transparency logs (via certstream) and attempts to find public S3 buckets from permutations of the certificates domain name.

**Prerequisites** 
* Provide AWS secrets in config.yaml as this greatly speeds up the checking rate.
* Python requirements installed.

**Key features**
* If you provide AWS access and secret keys in config.yaml Bucket Stream will attempt to access authenticated buckets and identity the buckets owner. Unauthenticated users are severely rate limited.
* Find interesting Amazon S3 Buckets by watching certificate transparency logs.

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/BucketStream_1.png)

