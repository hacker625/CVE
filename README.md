# EaseUS MobiMover 6.0.5 Build 21620 - Insecure Files and Folders Permissions
MobiMoverUILaunch.exe  suffers from an elevation of privileges vulnerability which can be used by an "Authenticated User" to modify the executable file of the service with a binary of his choice under bin folder . The vulnerability exist due to weak set of permissions being granted to the "Authenticated Users Group" which grants the (M) Flag aka "Modify Privilege"

Date: 2023-02-1
Author: Min Ko Ko (Creatigon)
Vendor Homepage: https://www.easeus.com/
Software Link : https://down.easeus.com/product/mobimover_trial_setup
Website : https://creatigon.com
Tested on: Microsoft Windows 10 Pro 10.0.10240 N/A Build 10240
POC video: https://www.youtube.com/watch?v=FR4cQm-z4Gw
