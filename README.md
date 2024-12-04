## debloating

https://rentry.org/debloatguide

## useful tools
[Explorer Patcher](https://github.com/valinet/ExplorerPatcher)

[Defender Control](https://github.com/qtkite/defender-control)

[Microsoft Activation Scripts (MAS)](https://github.com/massgravel/Microsoft-Activation-Scripts)

[PowerToys](https://github.com/microsoft/PowerToys)

## remove windows defender
[yep you heard that right](https://lazyadmin.nl/win-11/turn-off-windows-defender-windows-11-permanently/)

## install malwarebytes

https://rentry.org/MB-Premium/

## uninstall microsoft edge

https://rentry.org/uninstall_edge

## windows media player plus plugin

https://bmproductions.fixnum.org/index.htm?https://bmproductions.fixnum.org/wmpplus/

## install windows store on ltsc systems

wsreset -i

## restore windows photo viewer

https://github.com/peterweissbier/Restore_Windows_Photo_Viewer

## disable "windows protected your PC"

1. search for "reputation based protection"
2. disable "check apps and files"

## disable "these files might be harmful to your computer"

https://www.makeuseof.com/windows-disable-these-files-might-harmful-computer/

## disable "The publisher could not be verified, Are you sure you want to run this software"

https://www.thewindowsclub.com/the-publisher-could-not-be-verified

## disable unsafe file prompt

1. search for "inetcpl.cpl" and press enter
2. in the security tab, click 'custom Level'
3. enable "launching applications and unsafe files"
4. restart

## bypass "this PC can’t run Windows 11"

1. on "this PC can't run Windows 11" click on the arrow to go a step back
2. Shift-F10 to open the cmd
3. type "regedit"
4. create registry keys via navigating to HKEY_LOCAL_MACHINE\SYSTEM\Setup
<pre style="margin-bottom: 0; border-bottom:none; padding-bottom:0.8em;">--> Create a new Key with the name LabConfig
--> add the following DWORD (32-bit) Values and set the values to 1
BypassCPUCheck
BypassRAMCheck
BypassSecureBootCheck
BypassStorageCheck
BypassTPMCheck</pre>

5. close regedit and cmd and proceed with the installation

## bypass microsoft account (use offline account)

1. Disable internet connection
2. Shift-F10 to open the cmd
3. type oobe\bypassnro
4. after the reboot, select "i don't have internet" and "continue with limited setup"

## Make Windows 11 Accept File Paths over 260 Characters

1. open gpedit.msc

2.  browse to

Computer Configuration -> Administrative Templates -> System -> Filesystem

3. set Enable Win32 Long paths to enabled
