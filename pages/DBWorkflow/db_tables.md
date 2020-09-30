---
title: For Create Tables
keywords: For Create Tables
sidebar: dbwf_sidebar
permalink: db-development-workflow/for-create-tables.html
folder: DBWorkflow
hide_sidebar: false
comments: false
---

# For Create Tables

**Point 1**. Primary Key must be combination with **TenantID** and **key field**.

![](/images/primarykey.png) 

     1 (i). All PK should have TenantID+EntityID as primary key. But in large tables, use EntityID+TenantID as primary key to improve update query performance. 

![](/images/largetables.png)

     1 (ii). If EntityID is integer, and used in other tables, Primary key = EntityID+TenantID. 

![](/images/entityid.png)

     1 (iii). If EntityID is integer, and not used in other tables, Primary key = EntityID and EntityID is guid, Primary key = EntityID OK

![](/images/entityid-not-used.png)


**Point 2**.	TenantID must have default value & using this for default value **rls.fncGetTenantID ()** 

![](/images/defaultvalue.png)


**Point 3**.	Frist letter of all columns should be Capital and ID fields to be appear on top.
 
![](/images/capitalletter.png)

**Point 4**. Must be added require relationship for ID fields with combination TenantID like as FK.
 
![](/images/relationship.png)

     4 (i). All FK should have TenantID+EntityID as primary key. But in large tables, use EntityID+TenantID as primary key to improve update query performance.

![](/images/fk.png)


**Point 5**. Add Unique Constraints: *All unique indexes should have **TenantID** in it as last column.*
 
![](/images/uniqueconstraints.png)

**Point 6**. Applied proper Indexes for ID's field which are included in Join & where Conditions in functions & views and all indexes apart from primary index should not have TenantID column.

![](/images/index.png) 

![](/images/indexcolumn.png) 

![](/images/indexcolumns.png) 
 
 
**Point 7**. Created table should be included in tenantAccessPolicy (If it's Tenant Based)

![](/images/tenantaccesspolicy.png) 
 
**Point 8**. Assigned require permission to roles
 
     8 (i). Go to Database->Right click on Table and select Properties.

![](/images/tablerightclick.png) 
  
     8 (ii). Select Permissions  and click on Search button and click Browse button.

![](/images/permissions.png) 
 

     8 (iii). After click on Browse button Browse window open and marked on require objects(Roles, Users) and click on Ok.

![](/images/browse.png) 


     8 (iv). Now we can assigned require permission(Select/Delete/Insert/Update) click on Ok.
 
![](/images/tableproperty.png) 


**Point 9**. Synced with other Database where Table is require.   
 
![](/images/syncdb.png) 
