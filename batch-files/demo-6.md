# Demo 6

We could also prompt the user for values as the batch file is running. The **set** command can take input form the user to fill an environment variable. The **/P** switch prompts a user for input, this input is set to the environment variable.

```
:: Batch file to take arguments at runtime 
:: By: JOR
:: Initial file: 03JAN18
:: Filename: Demo6.bat

@echo off
cls
title JOR’s user prompt test
echo *******************************************
echo Welcome 
echo This batch file will do stuff
echo This is for demonstration purposes only.
echo *******************************************

set /p NAME=What is your name?
echo Your name is %NAME%
```

<figure><img src="https://www.gitbook.com/cdn-cgi/image/dpr=2,width=760,onerror=redirect,format=auto/https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2FlMaoRlx9Xkw6lfxweTIh%2Fblobs%2FaNKr5my9kYn9bP3KEK9k%2Fimage.png" alt=""><figcaption></figcaption></figure>
