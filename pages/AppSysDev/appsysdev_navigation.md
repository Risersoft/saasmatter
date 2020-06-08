---
title: Navigation
keywords: Navigation
sidebar: appsysdev_sidebar
permalink: appsystem-developer/navigation.html
folder: AppSysDev
hide_sidebar: false
comments: false
---

# Navigation

## Create

Click on New-> New Navigation

![](/images/navigation.jpg)

**Application** ->User can select application in this block.
**
**Product**** ->User can set product for created Navigation in this block.

**Nav Code** ->User can set Code for created Navigation.it is **unique** for publisher and product.

**Sortindex** ->User can sortindex for created navigation it i**s require sequencing for right click option.

**Nav Caption** ->User can set display name for created navigation in this block.

>Application Tab

**Platforms** -> User can set platform for created form like window, web etc.

**Menu** ->Menu block include two parts.

**Menu Tag** ->User can menu definition for navigation in this block.

![](/images/menutag.jpg)

**Menu Category** ->User can set menu category in this block like
Nav for navigation.

Currently using three type of navigation.

**(i)**.nav—For Navigation

**(ii)**.adfrm->For Add Option.

**(iii)**.editfrm->For Edit Option  

![](/images/menucategory.jpg)

> Conditions Tab

![](/images/conditionstab.jpg)

**View Condition** ->User can set view in this block.Created navigation Showing on only this.

>DataXML Tab  

![](/images/dataxmltab.jpg)

**SysEntXML**->User can set Idfield in this block, Created Navigation visible only if this idfield available on view.

    E.g. <SYS ID="CompanyID"/>

**Grid Condition**->User can set condition in this block. Created navigation available only if this condition full fill.

    E.g. <COL KEY="DocType"><VALUE VALUE1="IS"/></COL>

>Children Tab

![](/images/navigationchildrentab.jpg)

##  List

Click on Appsystem->Navigation

![](/images/navigationlist.jpg)

## Edit

Click on Appsystem->Navigation->Right Click->Edit Navigation

![](/images/editnavigation.jpg)
