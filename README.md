# MDT Deploy Applications
This aren't powershell script, but a collection of scripts I used for my MDT deployments. I figured it could be useful for others.

## Project: 
 - This is part of my MDT automation Project

## What it does:
<br>I have all my MDT applications seperated into individual folders all have a source folder and config folder. Not all of them use hte config folder. Some of the applications use an additional version folder. 

## Works on:
 - Only updates products that are download usign this script (https://github.com/PowerShellCrack/Get3rdPartySoftware)
 

 ## Steps:
 
  1. I use my 3rdPartyDownload script (https://github.com/PowerShellCrack/Get3rdPartySoftware) to download the software and place them in the folder 
     
  2. Then I run my MDTApplicationUpdater script (https://github.com/PowerShellCrack/MDTApplicationUpdater/tree/master) to update MDT's application.xml and corresponding wsf scripts versions 

## Future:
In time I will get it to update all the 3rd party applications (including office updates)
