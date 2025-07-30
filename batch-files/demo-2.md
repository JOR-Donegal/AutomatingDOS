# Demo 2

All commands which you run will display to the terminal and this can look messy. You can turn off this output by issuing the command **@echo off**

The **@** sign make the command apply to itself as well. We also have a minimum standard to apply headers, dates, etc. When we want to use comments, placing :: at the beginning of a line causes the line to be ignored.

```
:: Demo batch file to show a header and banner
:: By: JOR
:: Initial file: 03JAN18
:: Filename: Demo2.bat

@echo off
cls
title JOR’s first proper script
echo "*******************************************"
echo This batch file will do stuff
echo This is for demonstration purposes only.
echo "*******************************************"
```

<figure><img src="https://www.gitbook.com/cdn-cgi/image/dpr=2,width=760,onerror=redirect,format=auto/https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2FlMaoRlx9Xkw6lfxweTIh%2Fblobs%2FgnWSIrPxPTAXOVpWkqKW%2Fimage.png" alt=""><figcaption></figcaption></figure>
