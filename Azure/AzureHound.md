
## AzureHound uses graph theory to reveal the hidden and often unintended relationships within an Azure environment. 

AzureHound - https://bloodhound.readthedocs.io/en/latest/data-collection/azurehound.html

Attackers can use AzureHound to easily identify highly complex attack paths that would otherwise be impossible to quickly identify. Defenders can use AzureHound to identify and eliminate those same attack paths. 

**Prerequisites** 
* Az & AzureAD PowerShell modules
* User with at least Read access to the tenant and subscriptions.


**Key features**
* Collects data and displays it visually, includes shortest attack paths, valuable assets, users, groups and much more.
* As much of the screen real estate as possible is dedicated to the graph rendering area - where AzureHound displays nodes and the relationships between them.
* In the top left of the GUI is the search bar. Start typing the name of a node, and the GUI will automatically recommend nodes that match what you’ve typed so far. Click one of the suggestions, and the GUI will render that node.
* One of the most powerful features of AzureHound is its ability to find attack paths between two given nodes, if an attack path exists. 




![Import Module](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/AzureHound_1.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/AzureHound_2.png)


![Running The Script](https://github.com/JonathanScheinert/Cloud_PT_Tools/blob/main/Azure/Screenshots/AzureHound_3.png)
