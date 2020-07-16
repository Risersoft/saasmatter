---
title: Code Project Setup
keywords: Code Project Setup
sidebar: mvcwf_sidebar
permalink: web-development-workflow/code-project-setup.html
folder: Workflow
hide_sidebar: false
comments: false
---


# Code Project Setup

Prerequisite: Install Visual studio community in machine.

**Step 1**:

Accept invitation from your mail to access the Azure DevOps using your credentials.

Connect to the TFS server in visual studio using that server link which will be given on your mail.

![](/images/team-explorer.png)

**Step 2**:

Map & get the project in TFS and map to the
local path in system, you will map your projects on your system.

![](/images/tfs-map.png)

**Step 3**:

First of all download Dot net framework 4.7.2 and Dot net core 2.2 before build the project and change it in the properties of project in visual studio if it doesn’t effect.

**Dot net framework 4.7.2**:

https://dotnet.microsoft.com/download/dotnet-framework/net472

**Dot net core 2.2**:

https://dotnet.microsoft.com/download/dotnet-core/2.2

https://dotnet.microsoft.com/download/dotnet-framework/net472

#### Dot net framework 4.7.2:

![](/images/dot-net-framework-4.7.2.png)

#### Dot net core 2.2:

https://dotnet.microsoft.com/download/dotnet-core/2.2

![](/images/dot-net-core-2.2.png)

**Step 4**:

First open “rs.service.sln from auth folder” project, restore all NuGet packages, get latest version than rebuild, if you are facing references issue than open the project file in notepad.

please see below screenshot:

![](/images/restore-package.png)

**Step 5**: Install SQL server in machine.

**Step 6**: After map project look these screen

![](/images/team-explorer2.png)

**Step 8**: Open “rs.web.projects.sln”   get latest version then rebuild.

**Step 9**: Now get these screen

![](/images/solution-explorer.png)

**Step 10**: Check host file. You can get the hosts file from this location.

c:\Windows\System32\Drivers\etc\hosts.

![](/images/hosts.png)

**Step 11**: Before run projects set project properties.

**Step 12**: Now debug project then getting these screen.

![](/images/home-page.png)

**Step 13**: Now change url “**dev.test**” instead of “**localhost**”  then get these  screen.

![](/images/change-url.png)

**Step 14**→ Click on Start Now then open login page.

###### Some Important configurations for project execution

1. **applicationhost.config**

Open this file from execution location of the project

E.g. Path: ~ Projects\Talent\.vs\config
Remove the localhost text from bindinginformation for that site which you want to Run from the project’s list in solution explorer.

![](/images/application-host-config.png)

#### Service Bus Configuration:

****(String values are based on the Environment)**

**1)	For example, In Application GSTNirvana App dataConnectionstring.config**

##### Web Server Screen Shot:

![](/images/web-server.png)

#### Connection string will be:

 ****(String values are based on the Environment)**

<**connectionStrings**>  <add name="ServiceBus" connectionString="Endpoint=sb://its-mum-msg.servicebus.windows.net/;SharedAccessKeyName=RootManageSharedAccessKey;SharedAccessKey=55Du3F1hjuyrFujf25ayOU57UC3Vo84r1QBAlOd/GJ4= "/>
<**/connectionStrings**>

****Below screenshot of Azure to get the Service Bus Connection String:**

![](/images/azure.png)

Same as above application, below are the apps which required the Service Bus Configuration as per the environment.

2)	Service bus In AdminPortal --> App data--> Connectionstring.config

3)	Service bus In Agent --> App data--> Connectionstring.config

4)	Service bus In Hosted Agent-->  app.config

```
<connectionStrings>
    <add name="ServiceBus" connectionString="Endpoint=sb://its-mum-msg.servicebus.windows.net/;SharedAccessKeyName=RootManageSharedAccessKey;SharedAccessKey=55Du3F1hjuyrFujf25ayOU57UC3Vo84r1QBAlOd/GJ4=" />
    </connectionStrings>

```

5)	Service bus In Hosted Agent --> GSTNirvana.Agent.Hosted.exe.config

```
<connectionStrings>
    <add name="ServiceBus" connectionString="Endpoint=sb://its-mum-msg.servicebus.windows.net/;SharedAccessKeyName=RootManageSharedAccessKey;SharedAccessKey=55Du3F1hjuyrFujf25ayOU57UC3Vo84r1QBAlOd/GJ4=" />
</connectionStrings>

```

6)	Service bus In Hosted Agent -->  appsettings.json

```
{
  "ConnectionStrings": {
    "ServiceBus": "Endpoint=sb://its-mum-msg.servicebus.windows.net/;SharedAccessKeyName=RootManageSharedAccessKey;SharedAccessKey=55Du3F1hjuyrFujf25ayOU57UC3Vo84r1QBAlOd/GJ4="
  },

```


 ===========================**The End(Service Bus Entry)**====================


### $ Storage Account Configurations $


****(String values are based on The Environment)**

Storage Account Change in Application:

**For example Storage Account name** : itsmumstrg001

1)	In RegPortal--> App data--> Connection String

![](/images/connection-string.png)

The Connection String will be:

```
<connectionStrings>
<add name="Storage" connectionString="DefaultEndpointsProtocol=https;AccountName=itsmumstrg001;AccountKey=WA9I+RXdySGx3g05hUs6pibqJNu9Z7dH6AXlLR5Yrfb7rSQLj8Vp8Lb17u8Iwg5NqbynkET9LR6CD/KIe3to+Q== " />
</connectionStrings>

```

2)	For Storage account --In Database --> AuthDB2”Account Table”

****Change the Storage account value in “Storage account column”**

![](/images/account-table.png)

=========================The End (Storage Account)=========================
