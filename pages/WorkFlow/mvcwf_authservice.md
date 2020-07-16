---
title: Auth Service
keywords: Auth Service
sidebar: mvcwf_sidebar
permalink: web-development-workflow/auth-service.html
folder: Workflow
hide_sidebar: false
comments: false
---


# Auth Service

Our all applications use the Auth service for user authentication, which is hosted on our Server.
Application get reference for Login Auth service from “sitesettings.config” file.

**Step 1**:  “sitesettings.config” of Project for login service attribute.

We can provide the Auth service reference in Sitesetting.config file’s “authority” attribute.

We can provide the Auth service reference in Sitesetting.config file’s “authority” attribute.

```

<settings authority="http://login.qa.appsnirvana.com" clientId="lms.web" lientSecret="lmsweb123" publisherid ="ff35cdd7-33af-414f-a8a0-901e97d7f7b9"
publishername ="Risersoft" />

```

Authority for QA = http://login.qa.appsnirvana.com

Autority for Prod = http://login.risersoft.com

![](/images/auth-service-solution-explorer.png)


**Step 2**:  we hosted our Auth service on our server.

![](/images/auth-service-server.png)

Check “connectionstrings.config” and “sitesettings.config” of AuthorizationServerMulti

We can provide the database connection for Login in Auth project’s Connectionstring.config file and can modify it accordingly for QA and Prod


![](/images/auth-service-database.png)

For Login Authentication, need to change the connection string accordingly

**Path**:
 ~\AuthorizationServerMulti\App_Data\connectionstrings.config


```
<connectionStrings><add name="MaximpriseContext"
 connectionString="metadata=res://*/
 Entities.MaximpriseModel.csdl|res://*/
 Entities.MaximpriseModel.ssdl|res://*/
 Entities.MaximpriseModel.msl;provider=System.Data.SqlClient;
 provider connection string=&quot;data
 source=tcp:d2itschnsqldb01.database.windows.net,1433;Initial
 Catalog=Authdb2;user id=xyz;password=**********;Connection
 Timeout=90;MultipleActiveResultSets=False;App=EntityFramework
 &quot;" providerName="System.Data.EntityClient" /></
 connectionStrings>

```

**data source**: Provide the name of server/Elastic pool

**user id**: Provide the login user id of DB Server

**password**: Provide the DB Password
