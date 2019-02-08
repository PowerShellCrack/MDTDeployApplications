This aren't powershell script, but a collection of scripts I used for my MDT deployments. I figured it could be useful for others.

<br>I have all my MDT applications seperated into individual folders all have a source folder and config folder. Not all of them use rhte config folder. Some of the applciations use an additional version folder. This is becuse I use my 3rdPartyDownload script (https://github.com/PowerShellCrack/Get3rdPartySoftware) to download the software and place them in the folder while updating MDT's application.xml ()
