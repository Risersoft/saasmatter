---
title: IIS - Web Server Setup
keywords: IIS - Web Server Setup
sidebar: codeenv_sidebar
permalink: code-environment-setup/iis-web-server-setup.html
folder: CodeEnvSetup
hide_sidebar: false
comments: false
---

# IIS -Web server setup


1. Go to “Server Manager” and add the following roles & features:

![](/images/server-manager.png)

![](/images/server-manager-add-role.png)

![](/images/server-manager-add-role-install.png)

![](/images/server-manager-add-role-server-setup.png)


![](/images/server-manager-add-role-select-server-role.png)

![](/images/server-manager-add-role-server-feature.png)

2. Go to “IIS Manager”

3. Go to “Feature Delegation” and change features as follows:

![](/images/feature-designation.png)

![](/images/select-feature-designation.png)

4. For an example we can add the following sites as follows:

	a. AuthorizationServerMulti

	b. GstNirvana

![](/images/add-website.png)

![](/images/add-website-details.png)

5. Edit the site bindings as follows:

![](/images/edit-site-bindings.png)

a. AuthorizationServerMulti

![](/images/site-bindings.png)

b. GstNirvana

![](/images/site-binding.png)

8. Assign “Full Control” rights for “Everyone” group on “App_Data” folders of site.

![](/images/assign-rights.png)

9. Install complete “Web Deploy 3.6” from following URL:

https://www.microsoft.com/en-us/download/details.aspx?id=43717

10. **a) Configure “Management Service” as follows: (Windows Server version)**

![](/images/management-service.png)

![](/images/management-service2.png)

10. b) Configure “Management Service” as follows: (Windows non- Server version)

In Non-server versions of windows, the “Web Deployment Agent Service” should run in background for web deploy.

![](/images/management-service-non-server.png)

11. Configure “Management Service Delegation” as follows:

![](/images/management-service-delegation.png)

![](/images/management-service-delegation2.png)

12. Log in to the Azure portal, open the VM and select the “Networking” section & add following two inbound port rule in firewall entries:

	a. http - Port 80

  b. WebDeploy - Port 8172

![](/images/login-azure.png)

13. To use the in-built web publishing wizard in Visual Studio, the virtual machine must be configured with a DNS name. from the Azure portal, navigate to the “Overview” page of your virtual machine, under “DNS name”, click “Configure”, provide a globally unique DNS name. (A green tick appears when the name is validated.) & click Save to save the configuration:

![](/images/dns-server.png)

14. Follow the following article to setup publish profiles in Visual Studio projects:

https://github.com/aspnet/Tooling/blob/AspNetVMs/docs/publish-web-app-from-visual-studio.md
