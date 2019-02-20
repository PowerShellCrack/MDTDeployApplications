# MDT Deploy Applications
This aren't powershell script, but a collection of scripts I used for my MDT deployments. I figured it could be useful for others.

## Project: 
 - This is part of my <b>MDT automation Project</b>

## What it does:
<br>I have all my MDT applications seperated into individual folders
- all have a source folder and config folder. Not all of them use a config folder. 
- Some of the applications use an additional version folder. 

## Works on:
 - MDT/SCCM integration
 - This script (https://github.com/PowerShellCrack/Get3rdPartySoftware) will update the folder and script versions (see its list)
 - Logs most applications to _SMSTSLogs\AppLogs

## Steps:
 
  1. Use 3rdPartyDownload script (https://github.com/PowerShellCrack/Get3rdPartySoftware) to download the software 
     
  2. Run MDTApplicationUpdater script (https://github.com/PowerShellCrack/MDTApplicationUpdater/tree/master) and point it to the place the first script downloaded the software to. This will update MDT's application.xml and corresponding wsf scripts versions
   NOTE: make sure your MDT application is labeled by the product name and architecture. eg. Java x64

## Usage:
 - Build MDT applications and use command: cscript Install-<name>.wsf /arch:x64|x86
 - the <b>/arch</b> parameter are used fro applications that has both architectrue versions available. For intance, you can install Office 2016 32-bit or 64-bit on a 64-bit Windows. I have a application that has both version, but in different folders. To sepecify the right folder with writing two scripts I use the <b>/arch</b> parameter. 
 - If no <b>/arch</b> parameter is specified, it will use the OS architecture variable and if that can't be determined (not using MDT/SCCM), it defaults to x86
 
        eg. cscript Install-Office.wsf /arch:x86

## Future:
In time I want to get updates from all the 3rd party applications that I can think an enterprise use (including office updates)
