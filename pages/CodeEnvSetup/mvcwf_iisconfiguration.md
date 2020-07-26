---
title: IIS Configuration – For Hosted Agent
keywords: IIS Configuration – For Hosted Agent
sidebar: codeenv_sidebar
permalink: code-environment-setup/iis-configuration-for-hosted-agent.html
folder: CodeEnvSetup
hide_sidebar: false
comments: false
---

## IIS Configuration – For Hosted Agent

GSTNirvana.Agent.Hosted

![](/images/site-bindingsiss.png)

1. Edit the advanced settings of the “GSTNirvana.Agent.Hosted” site’s application pool as follows:

![](/images/advance-settings.png)

![](/images/advance-settings-details.png)

2. Edit the recycling settings of the “GSTNirvana.Agent.Hosted” site’s application pool as follows



![](/images/advance-settings-details2.png)

![](/images/application-pool.png)

![](/images/recycling-condition.png)

![](/images/recycling-event-to-log.png)

3. Edit the recycling settings of the “GSTNirvana.Agent.Hosted” site as follows:

![](/images/recycling-settings.png)

![](/images/recycling-settings-details.png)

4. Restart the “IIS Server” as follows:

![](/images/restart-server.png)

5. Assign “Full Control” rights for “Everyone” group on “App_Data” folders of site

![](/images/assign-rights3.png)

![](/images/assign-rights2.png)

6. Install “.NET Core 2.2 Runtime & Hosting Bundle” from following URL:

https://dotnet.microsoft.com/download/thank-you/dotnet-runtime-2.2.0-windows-hosting-bundle-installer

7. Run the following commands in an elevated (administrative privileged) command window:

net stop was /y

net start w3svc

**NOTE: If you don’t want to run the hosted agent, you need to stop the web site as well as application pool of it.**
