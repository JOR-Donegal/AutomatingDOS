# Demo 11

We can economically code in loop structures using the same “for” instruction that exists in many languages. To show what files are in a directory, you can type at the command prompt

```
FOR %F IN () DO @ECHO %F
```

Which means to pass all values of \* to the variable F and then echo them to the screen.\
We can do that with directories by using **/D**

```
FOR /D %D IN () DO @ECHO %D
```

The same thing works in a batch file EXCEPT you need to use a double **%%** to mark your variables.

```
:: Batch file to demonstrate loops 
:: By: JOR
:: Initial file: 03JAN18
:: Filename: Demo11.cmd

@echo off
cls
title JORs file and directory counter
echo *******************************************
echo This batch file will do stuff
echo This is for demonstration purposes only.
echo *******************************************

:: Iterate through all the files in the current directory
echo Analysing %CD%
FOR %%I IN (*) DO @ECHO Filename=%%I
echo *******************************************
:: The environment variable USERPROFILE points at the users home folder
echo Analysing %USERPROFILE% for directories
FOR /D %%I IN (%USERPROFILE%"\*") DO @ECHO %%I
echo *******************************************
```
