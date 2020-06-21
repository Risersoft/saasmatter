---
title: Delete Entity
keywords: Delete Entity
sidebar: mvcwf_sidebar
permalink: web-development-workflow/delete-entity.html
folder: Workflow
hide_sidebar: false
comments: false
---

## Delete Entity

This method is used to Delete an entity from Database. Use Delete query in place of Update to remove data permanently from table.

```



Public Overrides Function DeleteEntity(EntityKey As String, ID As Integer, AcceptWarning As Boolean) As clsProcOutput
        Dim oRet As New clsProcOutput
        Try
            If AcceptWarning Then
                Select Case EntityKey.Trim.ToLower
                    Case "email"
                        Dim sql As String = "Select * from Email Where EmailID =" & ID
Dim dt As DataTable = myContext.Provider.objSQLHelper.ExecuteDataset(CommandType.Text, sql).Tables(0)
                        If dt.Rows.Count > 0 Then
                            Dim sql1 As String = "update Email set IsDeleted= 'true', ModifiedByID='" & myContext.Police.UniqueUserID & "', LastUpdated='" & DateTime.Now & "'  where EmailID =" & ID
myContext.Provider.objSQLHelper.ExecuteNonQuery(CommandType.Text, sql1)
                        End If
                End Select
            ElseIf oRet.WarningCount = 0 Then
                oRet.AddWarning("Are you sure ?")
            End If
        Catch ex As Exception
            oRet.AddException(ex)
        End Try
        Return oRet
    End Function

```
