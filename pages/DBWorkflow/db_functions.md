---
title: For Create Functions
keywords: For Create Functions
sidebar: dbwf_sidebar
permalink: db-development-workflow/for-create-functions.html
folder: DBWorkflow
hide_sidebar: false
comments: false
---

# For Create Functions	

**Point 1**. Function name should be follow this pattern: **appcode+List+Tablename**

![](/images/table-valued-functions.png)

![](/images/viewfunction.png)  

**Point 2**. ID’s fields should be come on top in SQL.

![](/images/IDsintop.png) 
 
**Point 3**. All fields of parent table must be available in function.

![](/images/parenttable.png)  

**Point 4**. Description of code type fields should be lookup from codewords table.

![](/images/codeword.png)

![](/images/codewordtable.png)  


**Point 5**.	Check & verify all fields which are used in joins and where conditions should be applied indexes in respective tables.

![](/images/joins.png)
 
**Indexes**

![](/images/indexintable.png) 
 
**Point 6**. Check & verify Function's query do not take more time in execution. 

![](/images/functionexecute.png) 

**Point 7**. Key field of filter must be available in function which is available in applifilter of views which are based on created function.

![](/images/view.png) 

![](/images/filterkey.png) 

![](/images/executekey.png) 
  

**Point 8**. Include foreign key column in query instead of PK.
   
Eg: *AccvouchItem.GlaccountID instead of Glaccount.GlaccountID*.

![](/images/foreignkey.png) 
 

**Point 9**. Assigned Require permission to roles: Goto properties and click on Search and select roles by clicking on Browse option & assigned select permission for selected roles.

![](/images/modifyfunction.png) 

![](/images/functionproperties.png) 

![](/images/functionpermission.png) 
  