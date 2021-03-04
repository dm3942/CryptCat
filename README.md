# CryptCat
cryptcat is like netcat for windows with optional symmetric encryption using twofish.


# Requirements
Visual Studio Community 2019, install "Desktop development with C++" and ".NET desktop deployment".
Visual Studio is required for nmake.exe, cl.exe, linker.exe and a number of libraries.


# Compile
Start a command prompt, change directory then run nmake.exe

C:\>  
CD C:\PathToCode\cryptcat_nt_1.2.2\

C:\PathToCode\cryptcat_nt_1.2.2\ >
"c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\bin\Hostx64\x64\nmake.exe"


# Example Execution
How do you use it?

Local Test
----------
  Machine A: nc.exe -k SecretKeyUnderBobs -l -p 1234 < hobbit.txt

  Machine A: nc.exe -k SecretKeyUnderBobs 127.0.0.1 1234

Machine to Machine
------------------
  Machine A: nc.exe -k SecretKeyUnderBobs -l -p 1234 < hobbit.txt
    or 
  Machine A: nc.exe -k SecretKeyUnderBobs 127.0.0.1 1234


# Appendix
Compile output
--------------
Currently the output is very messy, standardization of the code is welcome.

C:\PathToCode\cryptcat_nt_1.2.2\ >
"c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\bin\Hostx64\x64\nmake.exe"

Microsoft (R) Program Maintenance Utility Version 14.28.29337.0
Copyright (C) Microsoft Corporation.  All rights reserved.

        "C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\bin\Hostx86\x86\cl.exe" /nologo /W3 /EHsc /O2 /D "NDEBUG" /D "WIN32" /D "_CONSOLE" /D "TELNET" /D "GAPING_SECURITY_HOLE" /FD /c /I"C:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\ucrt" /I"c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\include" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\um" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\shared" getopt.c
getopt.c
        "C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\bin\Hostx86\x86\cl.exe" /nologo /W3 /EHsc /O2 /D "NDEBUG" /D "WIN32" /D "_CONSOLE" /D "TELNET" /D "GAPING_SECURITY_HOLE" /FD /c /I"C:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\ucrt" /I"c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\include" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\um" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\shared" doexec.c
doexec.c
doexec.c(116): warning C4996: 'itoa': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _itoa. See online help for details.
doexec.c(124): warning C4996: 'itoa': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _itoa. See online help for details.
doexec.c(213): warning C4996: 'itoa': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _itoa. See online help for details.
doexec.c(229): warning C4996: 'itoa': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _itoa. See online help for details.
doexec.c(269): warning C4996: 'itoa': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _itoa. See online help for details.
doexec.c(344): warning C4996: 'itoa': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _itoa. See online help for details.
doexec.c(396): warning C4996: 'itoa': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _itoa. See online help for details.
        "C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\bin\Hostx86\x86\cl.exe" /nologo /W3 /EHsc /O2 /D "NDEBUG" /D "WIN32" /D "_CONSOLE" /D "TELNET" /D "GAPING_SECURITY_HOLE" /FD /c /I"C:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\ucrt" /I"c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\include" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\um" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\shared" netcat.c
netcat.c
netcat.c(93): warning C4005: 'EADDRINUSE': macro redefinition
C:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\ucrt\errno.h(85): note: see previous definition of 'EADDRINUSE'
netcat.c(94): warning C4005: 'ETIMEDOUT': macro redefinition
C:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\ucrt\errno.h(123): note: see previous definition of 'ETIMEDOUT'
netcat.c(95): warning C4005: 'ECONNREFUSED': macro redefinition
C:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\ucrt\errno.h(92): note: see previous definition of 'ECONNREFUSED'
netcat.c(368): warning C4996: '_sleep': This function or variable has been superceded by newer library or operating system functionality. Consider using Sleep instead. See online help for details.
netcat.c(489): warning C4996: 'strcmpi': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _strcmpi. See online help for details.
netcat.c(539): warning C4996: 'strcpy': This function or variable may be unsafe. Consider using strcpy_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(551): warning C4996: 'strncpy': This function or variable may be unsafe. Consider using strncpy_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(554): warning C4996: 'strncpy': This function or variable may be unsafe. Consider using strncpy_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(573): warning C4996: 'strncpy': This function or variable may be unsafe. Consider using strncpy_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(583): warning C4996: 'strncpy': This function or variable may be unsafe. Consider using strncpy_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(640): warning C4996: 'strncpy': This function or variable may be unsafe. Consider using strncpy_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(659): warning C4996: 'strncpy': This function or variable may be unsafe. Consider using strncpy_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(681): warning C4996: 'sprintf': This function or variable may be unsafe. Consider using sprintf_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(815): warning C4996: 'dup': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _dup. See online help for details.
netcat.c(855): warning C4996: '_sleep': This function or variable has been superceded by newer library or operating system functionality. Consider using Sleep instead. See online help for details.
netcat.c(1009): warning C4996: 'strcpy': This function or variable may be unsafe. Consider using strcpy_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(1011): warning C4996: 'strcat': This function or variable may be unsafe. Consider using strcat_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(1013): warning C4996: 'strcat': This function or variable may be unsafe. Consider using strcat_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(1014): warning C4996: 'strcat': This function or variable may be unsafe. Consider using strcat_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(1113): warning C4996: 'strcpy': This function or variable may be unsafe. Consider using strcpy_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(1125): warning C4996: 'strcpy': This function or variable may be unsafe. Consider using strcpy_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(1178): warning C4996: '_sleep': This function or variable has been superceded by newer library or operating system functionality. Consider using Sleep instead. See online help for details.
netcat.c(1275): warning C4996: 'sprintf': This function or variable may be unsafe. Consider using sprintf_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(1298): warning C4996: 'write': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _write. See online help for details.
netcat.c(1546): warning C4013: 'gets' undefined; assuming extern returning int
netcat.c(1547): warning C4996: 'strcat': This function or variable may be unsafe. Consider using strcat_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
netcat.c(1415): warning C4996: 'close': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _close. See online help for details.
netcat.c(1419): warning C4996: '_sleep': This function or variable has been superceded by newer library or operating system functionality. Consider using Sleep instead. See online help for details.
netcat.c(1544): warning C4996: 'kbhit': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _kbhit. See online help for details.
netcat.c(1555): warning C4996: 'close': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _close. See online help for details.
netcat.c(1560): warning C4996: 'read': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _read. See online help for details.
netcat.c(1562): warning C4996: 'close': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _close. See online help for details.
netcat.c(1570): warning C4996: 'close': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _close. See online help for details.
netcat.c(1592): warning C4996: 'write': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _write. See online help for details.
netcat.c(1620): warning C4996: '_sleep': This function or variable has been superceded by newer library or operating system functionality. Consider using Sleep instead. See online help for details.
netcat.c(1862): warning C4244: 'function': conversion from 'time_t' to 'unsigned int', possible loss of data
netcat.c(1713): warning C4996: 'read': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _read. See online help for details.
netcat.c(1867): warning C4996: 'close': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _close. See online help for details.
netcat.c(1873): warning C4996: 'open': The POSIX name for this item is deprecated. Instead, use the ISO C and C++ conformant name: _open. See online help for details.
netcat.c(2012): warning C4996: '_sleep': This function or variable has been superceded by newer library or operating system functionality. Consider using Sleep instead. See online help for details.
        "C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\bin\Hostx86\x86\cl.exe" /nologo /W3 /EHsc /O2 /D "NDEBUG" /D "WIN32" /D "_CONSOLE" /D "TELNET" /D "GAPING_SECURITY_HOLE" /FD /c /I"C:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\ucrt" /I"c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\include" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\um" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\shared" farm9crypt.cpp
farm9crypt.cpp
farm9crypt.cpp(145): warning C4996: 'sprintf': This function or variable may be unsafe. Consider using sprintf_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
        "C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\bin\Hostx86\x86\cl.exe" /nologo /W3 /EHsc /O2 /D "NDEBUG" /D "WIN32" /D "_CONSOLE" /D "TELNET" /D "GAPING_SECURITY_HOLE" /FD /c /I"C:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\ucrt" /I"c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\include" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\um" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\shared" twofish2.cpp
twofish2.cpp
twofish2.cpp(786): warning C4996: 'sprintf': This function or variable may be unsafe. Consider using sprintf_s instead. To disable deprecation, use _CRT_SECURE_NO_WARNINGS. See online help for details.
        "C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\bin\Hostx86\x86\link.exe" getopt.obj doexec.obj netcat.obj farm9crypt.obj twofish2.obj "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\ucrt\x86\libucrt.lib" "C:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\kernel32.Lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\user32.lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\wsock32.lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\winmm.lib" "c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\lib\x86\libcmt.lib" "c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\lib\x86\oldnames.lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\Uuid.Lib" "c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\lib\x86\libvcruntime.lib" /nologo /subsystem:console /machine:I386 /out:cryptcat.exe
