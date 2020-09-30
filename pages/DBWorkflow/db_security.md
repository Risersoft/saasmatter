---
title: Security
keywords: Security
sidebar: dbwf_sidebar
permalink: db-development-workflow/security.html
folder: DBWorkflow
hide_sidebar: false
comments: false
---

# Security	

**Point 1**. Check & verify on QA & Prod entries should be available in PublisherDBModule (Authdb) for created all DB's Users.

![](/images/users.png)

 
**Point 2**.	Check & verify on QA & Prod created users must be successfully login using dbuser & Dbpassword from PublisherDBModule.

*Goto->Database->Click on Connect->Enter Server Name, User & password as per PublisherDBModule and click on Options enter Database & then Connect*.

![](/images/publisherdbmodule.png)
 
**Point 3**.	If login failed then check entries in PublisherDB & PublisherDBModule if found mismatch then follow below steps (3.i & 3.ii) on QA & Prod.

![](/images/connect-to-server.png)
 
     3 (i). In Authdb2:Re-Set Password in PublisherDBModule table.

![](/images/resetpassword.png)
 
     3 (ii). In Database: Recreate user, using below steps. 

![](/images/recreateusers.png)

**Point 4**.	Roles must be moved to another database for tables/functions only not for users.

![](/images/moveroles.png)
 
**Point 5**.	All Roles membership file should be present in Users file in data project not in Role file.

![](/images/rolemembership.png)
