Usage
From the Windows Command Prompt
Compiling from the console isn't generally the most easy way of building software, but this explanation shows how you can get started quickly.

Open the Windows Command Prompt.
Make sure the mingw32/bin or mingw64/bin folder from the extracted download is in your PATH and its location doesn't contain any spaces.
Go to the directory where your source files are (C:\Temp in the example below).

SET PATH=D:\Prog\winlibs64-9.2.0-7.0.0\mingw64\bin;%PATH%
CD /D C:\TEMP

Create your source file(s) (helloworld.c in the example below).

NOTEPAD helloworld.c

In Notepad create the new file and then save it:

#include <stdio.h>

int main ()
{
  printf("Hello world!\n");
  return 0;
}

Compile the example:

gcc -o helloworld.exe helloworld.c

Or if you want to compile and link in seperate steps:

gcc -c -o helloworld.o helloworld.c
gcc -o helloworld.exe helloworld.o

Then you can run the compiled program:

helloworld.exe