# Demo 8

In most coding schemes, if we use **if** then we have operators. The operators in Windows are\


* EQU Equals to
* NEQ Not equal to
* LSS Less than
* LEQ Less than or equal to
* GTR Greater than
* GEQ Greater than or equal to

We also have _return values_. When a program runs successfully, it returns the value “0” to the operating system. Whenever it experiences an error, it returns a non-zero value and unfortunately, these are not well documented.

We can use the global environment variable **%ERRORLEVEL%** to see what the outcome of the last programme was. I will use brackets around my **IF** statement this time to make it a bit more elegant.

```
:: Demo batch file to configure something 
:: By: JOR
:: Initial file: 03JAN18
:: Filename: Demo8.bat

@echo off
cls
title JOR’s Error level tester
echo *******************************************
echo This batch file will do stuff
echo This is for demonstration purposes only.
echo *******************************************

SET ospath=C:\Windows\
SET filename=DoesNotExist.exe

:: The temp variable is defined globally for every user
Copy %ospath%%filename% %TEMP%

IF %ERRORLEVEL% NEQ 0 (
 echo The error level was %ERRORLEVEL% and that did not work.
)
```

<figure><img src="https://www.gitbook.com/cdn-cgi/image/dpr=2,width=760,onerror=redirect,format=auto/https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2FlMaoRlx9Xkw6lfxweTIh%2Fblobs%2FJFOL0SIXolM5mEmJqchF%2Fimage.png" alt=""><figcaption></figcaption></figure>

Notice that I got an error response from the command AND a response from my error checking.\
Although .bat and .cmd files have almost no distinctions, they may handle error levels a little differently.
