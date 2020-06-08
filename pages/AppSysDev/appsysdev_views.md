---
title: Views
keywords: Views
sidebar: appsysdev_sidebar
permalink: appsystem-developer/views.html
folder: AppSysDev
hide_sidebar: false
comments: false
---

# Views

## Create

There are two options to create views:
1. **New -> New View**
2. **AppSystem -> Views->Right Click ->Copy View..**

After choosing any one option, the View form will appear.

![](/images/createview.jpg)

**Product** -> Firstly select product in which views to be created.

    E.g- ASP

![](/images/viewproduct.jpg)

**Applications** ->  After select product than select applications.

    E.g-Kasp

![](/images/viewapplications.png)

**View Key** ->User can assign view key it is should be unique for Publisher and Product

    E.g-listInvoice

**StrView** ->User can set display name for view.

    E.g-Invoice

**Visualizations** ->User can select grid visualization for View output.

![](/images/viewvisualizations.png)

**Grid**->

![](/images/viewgrid.png)

**Chart**->

![](/images/viewchart.png)

**Dash**->

![](/images/viewdash.png)

**HTML**->

![](/images/viewhtml.jpg)

**Visualization Small** -> User can select grid visualization small for Mobile’s View output.

![](/images/viewvisualizationsmall.png)

**Grid**->                          **Chart**->

![](/images/viewgridchart.jpg)




**Dash**->     **List**->                   

![](/images/viewdashlist.jpg)



**Permission Key**-> User can set permission keys for created view.

    E.g-ID_SaleInvoices

![](/images/viewpermissionkey.png)

Default value is zero.

>DataSource Tab

User can set data source SQL for view output in this section.

![](/images/viewdatasourcetab.jpg)

**AppliFilters** ->User can set list of filters which are applicable on this view.

    E.g- Comp,Campus ..etc
![](/images/viewapplifilters.jpg)

**Type** ->User can set Data source query type Default value is Fields but user can it to Template as per requirement.

![](/images/viewtype.jpg)

**View Width Percent** ->User can set view’s output percentage.

    E.g-140.00

**Ignore Paging** ->Default value for this is False but user can set True if paging require on view output.

![](/images/viewignorepaging.jpg)

**Fields Tab** ->

![](/images/viewfieldstab.jpg)

**Select**-> User can set fields of Data source Query without select and Form keywords.

![](/images/viewselect.jpg)

**From**-> User can set Data Source Tables or Functions.

![](/images/viewfrom.png)

**Client**-> User can use Client if DataSoursce is PDCClientView

![](/images/viewclient.png)

**Group By**-> User can set Group by Fields of select query.

![](/images/viewgroupby.jpg)

**Having**-> If SQL query included Having Condition then user can set having condition in this section.

![](/images/viewhaving.png)

**Order BY**-> User can set Order columns in this section.

![](/images/vieworderby.png)

**Fixed Where**-> User can set fixed where conditions in this section.

![](/images/viewfixedwhere.jpg)

**ObjPermission**-> User can set Object which must be present in that Product.

>Generate->User can verify output of views after entered SQL query go to Grid available after Common tab then clicking on Generate Button and showing output.

![](/images/viewgenerate.jpg)

**Parameters Tab** ->

![](/images/parameterstab.jpg)

**FiltParam**-> User can set fixed filter with default value in this block.

**Note**: FiltParam should be in XML Code and use correct Syntax. If syntax not correct then errors showing in Errors block and applied Filters should be present in AppliFilters List.

    E.g.

![](/images/FiltParam.png)

**&lt;FILTER>** ->Starting Tag.

**FILTER KEY**->Set Filter key define in Table ClientFilter

**ACTION**->Set Default

**VALUE VALUE1**->Set IdField like FinyearID.Function Currfinid pick current finyearid.

**OPERTYPE**->Set operation type like eq for Equal.

**&lt;/FILTER>** ->Ending Tag.

**Output**->

![](/images/filteroutput.jpg)

**WhereParam** ->User can create Owen where conditions as per requirement and apply particular on menu’s in menu definition.

![](/images/WhereParam.png)

    E.g. Use WhereParam conditions in MenuDefination

![](/images/WhereParaminmenudifination.jpg)

**TransformBefore**-> TransformBefore worked before view output generated.

![](/images/TransformBefore.jpg)

    E.g. View Output before transformation.

![](/images/gridoutput.png)

![](/images/parametersoutput.jpg)

TARGET=0

**IDFIELD**->Assigned key field. Like Returnperiod

**PIVOT**->Assigned field to transform as header. Like SectionName

**AGGCOL**->Assigned field to transform below header respective SectionName. Like Amount

_View Output after transformation_:

![](/images/gridsummaryoutput.jpg)

**TransformAfter**-> TransformAfter worked after view output generate.

_View Output before transformation_ ->

![](/images/TransformAfter.jpg)

**ADDCOL** ->Column name which is to be added.

**KEY**->Assigned Caption name for added Field like perInc

**FORMULA**->Set value for Added column.

![](/images/formula.jpg)

_View Output after transformation_ ->

![](/images/formulaview.jpg)

>Common Tab

**ConditionXML**->

User can set print layout as per view output known as MMR.it is define in XML and follow below syntax.

![](/images/ConditionXML.jpg)

**FormatXML** -> User can format of columns of visible column like Caption, Date format etc.

![](/images/FormatXML.png)

**Output**:

![](/images/formatxmloutput.jpg)

**Print**->

![](/images/print.jpg)

**Print Vertical Grid Lines** ->Default value is null.

**Max Font Size** ->User can set font size of printing output.

**Filter for Printing** ->User can set filter which apply only when printing output.

**Hide Columns**->User cat set columns which are not require for printing.

**MMRXML**->User can define format for printing known as MMRXML.

    E.g.

![](/images/MMRXML.jpg)

**&lt;MMR>**->Starting Tag

**SERIAL** ->Set true if require serial number on MMR output.

**DETAILHTFACT **->Set row height for MMR output.

**HEADER PREFIX **->Set Header of MMR output.

**EVAL** ->Set Evaluate value like date

**FORMAT**->Set for mat of evaluate value.

**GROUP FIELD** ->Set Field name on which output should be group by.

**TYPE**->Set type of group by

**&lt;/MMR>** ->Ending Tag.

**Output**:

![](/images/MMRoutput.jpg)

>Grid Tab

**Complex** -> User can link multiple views through a key field in this section.

![](/images/complex.jpg)

**&lt;DISPGRID>** ->Starting tag

**&lt;/DISPGRID>** -> Ending tag

**&lt;MAINGRID>** ->Starting tag

**VIEW KEY** -> User can set view for display grid

**&lt;MAINGRID>** -> Ending tag

**&lt;MAKEREL INSERTAT** ->set default value 0.

 **BANDS** ->User can combine all child’s view in this section.

 **FIELD** ->Set idfield

 **CHILD** ->Set child using give value 1,2 etc.

![](/images/viewkey.jpg)

**Layout**-> User can define view layout in this section.

![](/images/layout.jpg)

**Inverted View**->User can marked if require visibility of columns horizontally.

**Ban Sort**->User can marked in require sorting on view.

**Reverse Direction**-> User can marked if require visibility of columns from Ending.

**Column Headers**->User marked if require fixed header.

**Fix Columns**-User can set fixed no of columns in this block.

**strWidth**->User can width for visible fields in this block.

**Heading Factor**->User can set width for header in this block.

**strBand**->User can set Display name for view.

**Row Height Factor**->user can set row height in this block.

**GroupOn**->User can set Group column Name in this block.

**Default Wid Fact.**->User can set default value of column’s width.

**Allow Group By**->User can marked if allow group by on header columns.

**Sort On Columns**->User can set columns require sorting on columns.

**Summary**->User can define summary totals for views in this block

![](/images/definesummary.jpg)

**Output** ->

![](/images/summaryoutput.jpg)

>Chart Tab

**ChartXML**->

![](/images/chartxml.jpg)

>Dashboard Tab

**HTML**->

![](/images/html.jpg)

**DashBoardXML**->

![](/images/DashBoardXML.png)

>Totals Tab

**TotalsXML**->

![](/images/TotalsXML.jpg)

**Output** ->

![](/images/totalsxmloutput.jpg)

>List Tab

User can define mobile views output in this block.

![](/images/listtab.jpg)

>Children Tab


![](/images/viewchildrentab.jpg)

## List

Click on AppSystem -> Applications->Views

![](/images/viewlist.jpg)


## Edit

Click on AppSystem -> Applications->Right Click->Edit In View Designer

![](/images/editview.jpg)
