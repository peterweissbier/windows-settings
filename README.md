## debloating

https://rentry.org/debloatguide

## useful tools

[Disable Windows Defenderl](https://github.com/es3n1n/defendnot)

[Activate Windows and Office with Microsoft Activation Scripts (MAS) tool](https://github.com/massgravel/Microsoft-Activation-Scripts)

[PowerToys](https://github.com/microsoft/PowerToys)

## completely remove windows defender
https://lazyadmin.nl/win-11/turn-off-windows-defender-windows-11-permanently/

## setting up Comic Sans MS as the primary font

https://github.com/peterweissbier/comicsans

## install malwarebytes

https://rentry.org/MB-Premium/

## uninstall microsoft edge

https://rentry.org/uninstall_edge

## windows media player plus plugin

https://bmproductions.fixnum.org/index.htm?https://bmproductions.fixnum.org/wmpplus/

## install windows store on ltsc systems

wsreset -i

## disable "windows protected your PC"

1. search for "reputation based protection"
2. disable "check apps and files"

## disable "these files might be harmful to your computer"

https://www.sevenforums.com/tutorials/182353-open-file-security-warning-enable-disable.html

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

## Bring the old Windows 10 context menu back on Windows 11

execute this in a terminal and restart the file explorer 
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
