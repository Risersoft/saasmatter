---
title: Pattern 3
keywords: Pattern 3
sidebar: winwf_sidebar
permalink: windows-development-workflow/pattern3.html
folder: WinWorkflow
hide_sidebar: false
comments: false
---
# Pattern 3

Template/Schema/Importer :-

**1. Templates** :- These are excel files for each and every importer.

It is a Customer Template where fields are defined of the tables where data to be inserted.

![](/images/template.png)

**2. Schema** :- it is a xml file where Database table fields are mapped with the excel template fields.

![](/images/schema.png)

-	Here in RecordType tag -> Name of the template is defined i.e. Customer Master.

-	After that fields are defined in Name tag

-	In Description tag the description to be shown in the template is defined

-	Datatype fields -> defines the datatype of the field

-	Level = 1 i.e. Main Table field, Level =2 i.e. child table field.

-	If field is Mandatory then True else False.


**3. Importers** :-  Import_CustomerTaskProvider

Firstly packages are defined for import then class is defined after that PartyType and PartySubType is defined. For here PartyType = ‘C’ and PartySubTypeTable = ‘Customer’.

![](/images/importers.png)

**-->** DocType, TemplateName, TemplateFunctionName is defined.

![](/images/importers2.png)

**-->** ExecutePreValidation Function :- here prevalidations are executed.

![](/images/execute_prevalidate_function.png)

**-->** Execute Server and FindVouch Function :-

![](/images/execute_function.png)

This class inherits ->  ImportTaskProviderPartyBase

**GenerateSQL function** :-

![](/images/generate_sql_function.png)

HandleGroupData Function :-

![](/images/handle_group_data_function.png)

![](/images/handle_group_data_function2.png)

![](/images/handle_group_data_function3.png)

![](/images/handle_group_data_function4.png)

![](/images/handle_group_data_function5.png)

![](/images/handle_group_data_function6.png)

![](/images/handle_group_data_function7.png)

![](/images/handle_group_data_function8.png)


**TryImportRowGroup Function** :-

![](/images/try_import_row_group.png)

![](/images/try_import_row_group2.png)

![](/images/try_import_row_group3.png)


**3.2**	If the excel file is not reading then we have to check *Excel Sheet Name* and *TemplateName* in the Import Provider are same or not if not same it will not read the data in the excel file.

**3.3**	If the above condition is true and still Importer is not able to read the data then we have to check whether the excel sheet contains the Columns -> *Warning Code, Warning Descriptions, Error Code and Error Descriptions.*
