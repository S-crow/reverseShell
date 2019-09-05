# Simple reverse shell on a target machine using C# code and bypassing AV solutions  

## Compile code to .exe
sudo apt install mono-complete
mcs -out:hello.exe hello.cs
mono hello.exe
