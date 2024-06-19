## bypass "this PC can’t run Windows 11"

1. on "this PC can't run Windows 11" click on the arrow to go a step back
2. Shift-F10 to open the cmd
3. type regedit
4. create registry keys via navigating to HKEY_LOCAL_MACHINE\SYSTEM\Setup
   --> Create a new Key with the name LabConfig
   --> add the following DWORD (32-bit) Values and set the value to 1

<pre style="margin-bottom: 0; border-bottom:none; padding-bottom:0.8em;">BypassCPUCheck
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
