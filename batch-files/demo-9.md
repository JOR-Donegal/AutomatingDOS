# Demo 9

There is a shortcut way to show success or failure. If a command is successful, we can use the && command to execute a follow-on command. If a command fails, we can use **||** to execute a follow-on command.

```
:: Batch file to display success or failure 
:: By: JOR
:: Initial file: 03JAN18
:: Filename: Demo9.bat

@echo off
cls
title JOR’s Error level tester v.2
echo *******************************************
echo This batch file will do stuff
echo This is for demonstration purposes only.
echo *******************************************

SET ospath=C:\Windows\
SET filename1=explorer.exe
SET filename2=DoesNotExist.exe
copy %ospath%%filename1% %TEMP% && echo Copy of %filename1% worked!
echo.
echo.
copy %ospath%%filename2% %TEMP% || echo Copy of %filename2% failed!
```

I wanted to have clear space between the two actions, **echo.** achieved that for me.

<figure><img src="https://www.gitbook.com/cdn-cgi/image/dpr=2,width=760,onerror=redirect,format=auto/https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2FlMaoRlx9Xkw6lfxweTIh%2Fblobs%2FvEr57NMAd339mk9tqtDa%2Fimage.png" alt=""><figcaption></figcaption></figure>

One useful modification of this is to halt a script if it experiences an error. If I get an error, I want to exit the script, but I don’t want to close the command shell; **/B** achieves that for me.

I want to return an error code; I can append a code to the exit command, and this will be returned to the operating system. In this case, I am returning the value 1.

```
copy %ospath%%filename2% %TEMP% || echo EXIT /B 1
```

I could of course create my own error levels for use in the script. That way, every error return code would have a specific meaning.

```
SET /A ERROR-FileNotFound=1
SET /A ERROR-DirectoryNotFound=2
SET /A ERROR-Undefined=3
```
