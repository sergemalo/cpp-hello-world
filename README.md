# cpp-hello-world
C++ Hello World program

## Compiler
I chose to use MinGW. It contains the gdb debugger
I selected this file: [x86_64-14.2.0-release-win32-seh-ucrt-rt_v12-rev1.7z](https://github.com/niXman/mingw-builds-binaries/releases/download/14.2.0-rt_v12-rev1/x86_64-14.2.0-release-win32-seh-ucrt-rt_v12-rev1.7z)
Just unzip to c:\mingw64\  

## Linking error
To fix the basic link error, I needed to tell Studio Code to use g++ instead of gcc.  
See "tasks.json" file of the project:  
 ```           "command": "C:/mingw64/bin/g++.exe",```



### Selecting the right MinGW (notes from ChatGPT)

To choose the correct version, consider the following factors:

Architecture: Do you have a 32-bit (i686) or 64-bit (x86_64) system?
Thread model: Do you want to use the POSIX thread model or the Win32 thread model?
Exception model: Do you want to use the Dwarf exception model or the SEH (Structured Exception Handling) exception model?
CRT (C Runtime): Do you want to use the MSVCRT (Microsoft Visual C++ Runtime) or the UCRT (Universal C Runtime)?
Based on your original question, I assume you're on a 64-bit Windows system. In that case, I recommend the following:

x86_64-14.2.0-release-win32-seh-ucrt-rt_v12-rev1.7z (86.4 MB)
This version is suitable for most use cases:

64-bit architecture (x86_64)
Win32 thread model ( compatible with most Windows APIs)
SEH exception model (compatible with most Windows applications)
UCRT (Universal C Runtime) for better compatibility with modern Windows systems