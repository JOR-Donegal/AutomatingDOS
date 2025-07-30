# Demo 4

Variables are very useful for making a batch file readable and reusable. You need to be careful as any variables you set will remain set once the batch file is finished. It might be a good idea to use SETLOCAL/ENDLOCAL to prevent this. Also, do not put any spaces between the variable name and the value.

By convention, variables which are local to the script are kept as lower case.\
Variables which are global are upper case.\
We can also do calculations with SET also.

```
:: Batch file to demonstrate variables
:: By: JOR
:: Initial file: 03JAN18
:: Filename: Demo4.bat

@echo off
cls
title JOR’s variable test
echo *******************************************
echo This batch file will do stuff
echo This is for demonstration purposes only.
echo *******************************************

echo *** About to do something critical ***
echo *** press [ctrl][c] to exit or any key to continue ***
pause 

SETLOCAL

SET clonepath=V:\Clone of UB1604-Server\
SET clonename=UB1604-04JAN18.vmx
echo Path to Clone is %clonepath%%clonename%

SET /A calculation=2+12/4
echo We got %calculation%

ENDLOCAL

EXIT
```

<figure><img src="https://www.gitbook.com/cdn-cgi/image/dpr=2,width=760,onerror=redirect,format=auto/https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2FlMaoRlx9Xkw6lfxweTIh%2Fblobs%2FFbPAV29iy2rTs8CK3gc6%2Fimage.png" alt=""><figcaption></figcaption></figure>
