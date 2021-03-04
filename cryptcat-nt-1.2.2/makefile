
cc="C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\bin\Hostx86\x86\cl.exe"
link="C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\bin\Hostx86\x86\link.exe"

incs="C:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\ucrt\stdio.h" 

cflags=/nologo /W3 /EHsc /O2 /D "NDEBUG" /D "WIN32" /D "_CONSOLE" /D "TELNET" /D "GAPING_SECURITY_HOLE" /FD /c /I"C:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\ucrt" /I"c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\include" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\um" /I"c:\Program Files (x86)\Windows Kits\10\Include\10.0.18362.0\shared"
lflags="c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\ucrt\x86\libucrt.lib" "C:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\kernel32.Lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\user32.lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\wsock32.lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\winmm.lib" "c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\lib\x86\libcmt.lib" "c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\lib\x86\oldnames.lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\Uuid.Lib" "c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\lib\x86\libvcruntime.lib" /nologo /subsystem:console /machine:I386 /out:cryptcat.exe
lflagsnc="c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\ucrt\x86\libucrt.lib" "C:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\kernel32.Lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\user32.lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\wsock32.lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\winmm.lib" "c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\lib\x86\libcmt.lib" "c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\lib\x86\oldnames.lib" "c:\Program Files (x86)\Windows Kits\10\Lib\10.0.18362.0\um\x86\Uuid.Lib" "c:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.28.29333\lib\x86\libvcruntime.lib" /nologo /subsystem:console /machine:I386 /out:nc.exe

all: cryptcat.exe

getopt.obj: getopt.c
    $(cc) $(cflags) getopt.c

doexec.obj: doexec.c
    $(cc) $(cflags) doexec.c

netcat.obj: netcat.c
    $(cc) $(cflags) netcat.c

farm9crypt.obj: farm9crypt.cpp
    $(cc) $(cflags) farm9crypt.cpp

twofish2.obj: twofish2.cpp
    $(cc) $(cflags) twofish2.cpp

cryptcat.exe: getopt.obj doexec.obj netcat.obj farm9crypt.obj twofish2.obj
    $(link) getopt.obj doexec.obj netcat.obj farm9crypt.obj twofish2.obj $(lflags)

nc.exe: getopt.obj doexec.obj netcat.obj farm9crypt.obj twofish2.obj
    $(link) getopt.obj doexec.obj netcat.obj farm9crypt.obj twofish2.obj $(lflagsnc)
