---
title: Steps For Run HRMNirvana as Self Host Mode
keywords: Steps For Run HRMNirvana as Self Host Mode
sidebar: winwf_sidebar
permalink: windows-development-workflow/steps-for-run-hrmnirvana-as-self-host-mode.html
folder: WinWorkflow
hide_sidebar: false
comments: false
---


# Steps For Run HRMNirvana as Self Host Mode

**Step.1**: Firstly Change Connection String in C drive.Goto below path:
C:\Users\Username\AppData\Roaming\Risersoft\HRMNirvana\Edit Setting File and make Below Changes.

**Step.1. (a)**: Make **connstring** to **connstring2**

**Eg.  <connstring2> </connstring2>**

**Step.1. (b)**: Add below lines and Connection file saved.

```
  <authority>http://login.risersoft.com</authority>
  <self-clientid>hrm.web</self-clientid>
  <self-clientSecret>hrmweb123</self-clientSecret>
  <selfhost>true</selfhost>

```

![](/images/step-host.png)

**Step.2**: Now run Visual studio as Administrator


**Step.3**: Now appearing Login window, Enter username & Password and click on Login.
