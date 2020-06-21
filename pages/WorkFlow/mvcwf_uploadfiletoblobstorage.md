---
title: Upload File to BLOB Storage
keywords: Upload File to BLOB Storage
sidebar: mvcwf_sidebar
permalink: web-development-workflow/upload-file-to-blob-storage.html
folder: Workflow
hide_sidebar: false
comments: false
---
## Upload File to BLOB Storage

Upload file on cloud storage using below code.

```



Public Overrides Function GenerateParamsOutput(dataKey As String, Params As List(Of clsSQLParam)) As clsProcOutput
Dim _NewFileName As String = myUtils.cStrTN(myContext.SQL.ParamValue("@filename", Params))
   Dim oRet As New clsProcOutput
   Select Case dataKey.Trim.ToLower
      Case "sas"
      Dim OrigFileName = Path.GetFileNameWithoutExtension(_NewFileName)
_NewFileName = OrigFileName + "--" + Guid.NewGuid.ToString + Path.GetExtension(_NewFileName)
      Dim provider As New clsBlobFileProvider(myContext)
      Dim container = myPathUtils.GetContainerName(myContext)
      Dim oRet2 = provider.CreateUploadUri(container, _NewFileName, "")
      If oRet2.Success Then
oRet.JsonData = New With {.status = 200, .success = oRet.Success, .message = oRet.Message, .Data = oRet2.Result.Uri.ToString, .flName = _NewFileName}
      Else
oRet.JsonData = New With {.status = 200, .success = oRet.Success, .message = oRet.Message} '"Unable to upload file."
      End If
   End Select
   Return oRet
End Function

```
