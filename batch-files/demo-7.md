# Demo 7

To make our scripts more powerful, we can use the if/else constructs which most programming languages have. The format is the familiar **if&#x20;**_**condition command**_

We can also use negation in **if not&#x20;**_**condition command**_

```
:: Batch file to demonstrate conditional branching 
:: By: JOR
:: Initial file: 03JAN18
:: Filename: Demo7.bat

@echo off
cls
title JOR’s Find a File
echo *******************************************
echo This batch file will do stuff
echo This is for demonstration purposes only.
echo *******************************************

SET ospath=C:\Windows\
SET filename=explorer.exe

If exist %ospath%%filename% echo %filename% exists 
```

<figure><img src="https://www.gitbook.com/cdn-cgi/image/dpr=2,width=760,onerror=redirect,format=auto/https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2FlMaoRlx9Xkw6lfxweTIh%2Fblobs%2FYuS3IVvLedsvxR1v0D7O%2Fimage.png" alt=""><figcaption></figcaption></figure>

Whenever we use **if** we normally have an alternative **else**. These can be coded with braces for readability. We can also have multiple lines of commands for both alternatives.

```
If exist %ospath%%filename% (
	echo %filename% exists
) else (
	echo No file named %filename%
)
```
