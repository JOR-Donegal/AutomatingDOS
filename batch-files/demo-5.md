# Demo 5

Rather than predefining variables, we can let some user pass parameters as they are running the code. These parameters are called arguments, and are passed as %1, %2

I have commented out the cls so you can see the program in its entirety.

Note that you can only pass variables for 0-9.

```
:: Batch file to demonstrate arguments 
:: By: JOR
:: Initial file: 03JAN18
:: Filename: Demo5.bat

@echo off
:: cls
Title JOR’s argument test
echo *******************************************
echo Welcome %1 %2
echo This batch file will do stuff
echo This is for demonstration purposes only.
echo *******************************************
```

<figure><img src="https://www.gitbook.com/cdn-cgi/image/dpr=2,width=760,onerror=redirect,format=auto/https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2FlMaoRlx9Xkw6lfxweTIh%2Fblobs%2F4p5ruBwHOsP7tJuqdZvb%2Fimage.png" alt=""><figcaption></figcaption></figure>
