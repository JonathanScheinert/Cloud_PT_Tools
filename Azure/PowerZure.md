PowerZure - https://github.com/hausec/PowerZure
## PowerZure is a PowerShell project created to assess and exploit resources within Microsoft’s cloud platform, Azure. PowerZure was created out of the need for a framework that can both perform reconnaissance and exploitation of Azure, AzureAD, and the associated resources.


**Prerequisites** 
* Az & AzureAD PowerShell modules
* User with at least Read access to the tenant and subscriptions.



**Key features**
* It is possible to extract users’ data, azure subscription information, harvest key vault values and much more. For example, type: Show-AzureCurrentUser to view the current signed-in user's roles in Azure and Azure AD. Also type Get-AzureTargets to compare your current signed-in user's roles and their scope to resources within Azure.

![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/PowerZure_1.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/PowerZure_2.png)
