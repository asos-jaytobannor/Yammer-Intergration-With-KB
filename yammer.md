# Yammer Intergration with knowledge base

This documentation will show how to connect a knowledge base with question and answer pairs with yammer . After the connection is made the result should be then when question is asked in a yammer community page a answer matching the question from the knowledge base should be retrived and shown as a reply to the orginal question. 

## Creating the knowledge base
Firstly the knowledge base (**KB**) need to be created. Log into azure portal and create a language resource which has the functionally to create a KB. Furthermore the Cognitive Services Contributor role need to be assigned to your account on the subscription you are using.

**Create language resource in Azure Cli**

```azurecli
az cognitiveservices account create --name <resource_name> --resource-group <resource_group> --kind TextAnalytics --sku F0 --location <region_name> --yes
```

After the language resource is created go to the overview section scroll down and you should **language studio** open it on a new tab.

In the language studio scroll down until you find **Custom Question Answering** and open it. Create a new project populate the fields inside containing the project name and source name. After the project is created add a **Azure Search Resource** to it (create a new one if there isn't a exsisting one).

