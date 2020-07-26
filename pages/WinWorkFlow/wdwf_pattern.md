---
title: Pattern 1
keywords: Pattern 1
sidebar: winwf_sidebar
permalink: windows-development-workflow/pattern1.html
folder: WinWorkflow
hide_sidebar: false
comments: false
---

# Pattern 1

1. **Multiselect function from a view and grid editable from different tables.**

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

2. **Softform of any form**

**-->** frmEwaybillPartB is the softform of frmewaybill.

**-->** SoftForm -> frmEwaybillPartB is called on the add and edit button of frmewaybill on Tab -> Part-B grid.

![](/images/softform_any_form.png)

![](/images/softform_any_form_code.png)

**-->** Code in frmEwaybillPartB :-

Declaration of the main form in the soft form as fMat.

![](/images/ewaybill.png)

**-->** PrepForm of softform :-

![](/images/prepform_of_softform.png)

Save & OK Button work :-

![](/images/save_ok_button.png)


