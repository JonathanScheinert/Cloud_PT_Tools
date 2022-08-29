
## DumpsterDiver is a tool, which can analyze big volumes of data in search of hardcoded secrets like keys (e.g., AWS Access Key, Azure Share Key or SSH keys) or passwords. 

DumpsterDiver - https://github.com/securing/DumpsterDiver

It allows creating a simple search rule with basic conditions (e.g., report only csv files including at least 10 email addresses). The main idea of this tool is to detect any potential secret leaks.

**Prerequisites** 
* To run the DumpsterDiver you have to install python libraries. You can do this by running the following command:
  * $ pip install -r requirements.txt


**Key features**
* Searches through git logs, unpacks compressed archives (e.g., zip, tar.gz etc.), supports advanced search using simple rules (details below), searches for hardcoded passwords and fully customizable.
* Can output file in JSON format

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/DumpsterDiver_1.png)

