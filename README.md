# EaseUS MobiMover 6.0.5 Build 21620 - Insecure Files and Folders Permissions
MobiMoverUILaunch.exe  suffers from an elevation of privileges vulnerability which can be used by an "Authenticated User" to modify the executable file of the service with a binary of his choice under bin folder . The vulnerability exist due to weak set of permissions being granted to the "Authenticated Users Group" which grants the (M) Flag aka "Modify Privilege"



Vendor Homepage: https://www.easeus.com/ <br/>
Software Link : https://down.easeus.com/product/mobimover_trial_setup<br/>
POC video: https://www.youtube.com/watch?v=FR4cQm-z4Gw


#PoC
```
C:\Users\creatigon>accesschk -uwvqd "C:\Program Files (x86)\EaseUS\EaseUS MobiMover\bin"

Accesschk v6.15 - Reports effective permissions for securable objects
Copyright (C) 2006-2022 Mark Russinovich
Sysinternals - www.sysinternals.com

C:\Program Files (x86)\EaseUS\EaseUS MobiMover\bin
  Medium Mandatory Level (Default) [No-Write-Up]
  RW BUILTIN\Users
        FILE_ALL_ACCESS
  RW NT SERVICE\TrustedInstaller
        FILE_ALL_ACCESS
  RW NT AUTHORITY\SYSTEM
        FILE_ALL_ACCESS
  RW BUILTIN\Administrators
        FILE_ALL_ACCESS
```
