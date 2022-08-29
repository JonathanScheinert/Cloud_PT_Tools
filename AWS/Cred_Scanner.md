
## A simple command line tool for finding AWS credentials in files. 

cred_scanner - https://github.com/disruptops/cred_scanner

Optimized for use with Jenkins and other CI systems. I suspect there are other, better tools out there (such as git-secrets), but I couldn't find anything to run a quick and dirty scan that also integrates well with Jenkins.

**Prerequisites** 
* Python requirements installed.

**Key features**
* Will scan the local directory or provided path and all subdirectories within that path. It will list the files, which have potential access keys, and which files can't be scanned due to the file format. cred_scanner exits with a code of 1 if it finds any potential keys.
* On a Compromised EC2 instance, this is a useful tool to extract secrets.

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/CredScanner_1.png)


