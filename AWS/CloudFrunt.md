
## CloudFrunt is a tool for identifying misconfigured CloudFront domains. 

CloudFrunt - https://github.com/MindPointGroup/cloudfrunt

When a CloudFront endpoint receives a request, it does NOT automatically serve content from the corresponding distribution. Instead, CloudFront uses the HOST header of the request to determine which distribution to use. This means two things:
If the HOST header does not match an entry in the "Alternate Domain Names (CNAMEs)" field of the intended distribution, the request will fail.
Any other distribution that contains the specific domain in the HOST header will receive the request and respond to it normally.
This is what allows the domains to be hijacked. There are many cases where a CloudFront user fails to list all the necessary domains that might be received in the HOST header. 

**Prerequisites** 
* Git clone the tool from the GitHub repository and make sure that dnsreacon tool exist as a subdirectory.
* Python requirements installed.
* Customized wordlists to enumerate subdomains.

**Key features**
* Attempts to hijack misconfigured CloudFront subdomains of an organization.
* Able to use a wordlist of your choice.

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/AWS/Screenshots/CloudFrunt_1.png)

