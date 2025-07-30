# Demo 10

In almost all command line environments, we have the concept of;

1. A standard input device, normally the keyboard (STDIN=0)
2. A standard output device, normally the screen (STDOUT=1)
3. A standard error device, also normally the screen (STDERR=2)

You may have seen these in the Linux shell and we can also use them in Windows/DOS. At the command prompt, try typing **DIR > rubbish.txt** and check what happened. You should have a new file called **rubbish.txt** with whatever the output of the DIR command was. We have redirected the output of a command to a file using the operator >. This operator will create or overwrite the file.

If we use the **>>** operator, it will append to the file. In this way, we can create our own log files.

We could also use numbers to describe the I/O and we can combine redirects. If I want to send both the output AND the error output to a file I could use the operator combination **2>&1**

```
:: Batch file to demonstrate redirection
:: By: JOR
:: Initial file: 03JAN18
:: Filename: Demo10.cmd

@echo off
cls
title JORs simple backup with logging
echo *******************************************
echo This batch file will do stuff
echo This is for demonstration purposes only.
echo *******************************************

:: Create a blank file or erase it if it already exists
echo *** Demo10 Logfile *** > SimpleBackup.log

SET ospath=C:\Windows\
SET filename1=explorer.exe
SET filename2=DoesNotExist.exe

echo 1. Copying %filename1% >> SimpleBackup.log
copy %ospath%%filename1% %TEMP% >> SimpleBackup.log 2>&1
echo 2. Copying %filename2% >> SimpleBackup.log
copy %ospath%%filename2% %TEMP% >> SimpleBackup.log 2>&1
```

<figure><img src="https://www.gitbook.com/cdn-cgi/image/dpr=2,width=760,onerror=redirect,format=auto/https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2FlMaoRlx9Xkw6lfxweTIh%2Fblobs%2FUGH32IIkCTRPgmdsIZ8O%2Fimage.png" alt=""><figcaption></figcaption></figure>

If you need to redirect output down a black hole, you can use the NUL device. The command DIR > NUL will suppress any output to the screen. For old hands at the command prompt, we could create files without an editor by redirecting cmd.exe’s STDIN to a file. I can create a file called text.txt by copying it from the console.

```
JOR> copy con test.txt
This is a test file
^Z
JOR>
```

We use **\[ctrl]\[z]** to close the file.
