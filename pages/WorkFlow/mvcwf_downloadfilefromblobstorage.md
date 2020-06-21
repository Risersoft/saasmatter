---
title: Download File From BLOB Storage
keywords: Download File From BLOB Storage
sidebar: mvcwf_sidebar
permalink: web-development-workflow/download-file-from-blob-storage.html
folder: Workflow
hide_sidebar: false
comments: false
---

## Download File From BLOB Storage

To download file from cloud storage you need Filename and Container name.

```

Public Overrides Function GenerateParamsOutput(dataKey As String, Params As List(Of clsSQLParam)) As clsProcOutput
Dim _NewFileName As String = myUtils.cStrTN(myContext.SQL.ParamValue("@filename", Params))
        Dim oRet As New clsProcOutput
        Select Case dataKey.Trim.ToLower
            Case "download"
                Dim provider As New clsBlobFileProvider(myContext)
                Dim container = myPathUtils.GetContainerName(myContext)
                Dim oRet2 = provider.GetDownloadUri(container, _NewFileName)
                If oRet2.Success Then
oRet.JsonData = New With {.status = 200, .success = oRet.Success, .message = oRet.Message, .Data = oRet2.Result.Uri.ToString}
                Else
oRet.JsonData = New With {.status = 200, .success = oRet.Success, .message = oRet.Message} '"Unable to upload file."
                End If
        End Select
        Return oRet
    End Function

```
