---
title: Multiselect function
keywords: Multiselect function
sidebar: winwf_sidebar
permalink: windows-development-workflow/multiselect-function.html
folder: WinWorkflow
hide_sidebar: false
comments: false
---


**Multiselect function from a view and grid editable from different tables.**

   Multiselect applied on the **Grid -> Member** on Add Member Button.

![](/images/multiselect_function.png)

**-->**	Code in **frmCommittee -> AdvancedSelect** function called in the button Add Member, Screenshot attached.

![](/images/advance_select.png)

**-->** Grid binding done in **frmCommitteeModel** :-

### Prepform :-

![](/images/prepform.png)

**--> GenerateParamsModel Function :-**

![](/images/generate_params.png)

Sorting done by Moveup, MoveDown, Renumber buttons. By code :-

oSort = New clsWinSort(myView, Me.btnMoveup, Me.btnMoveDown, btnRenumber, "rank")

![](/images/committee.png)
