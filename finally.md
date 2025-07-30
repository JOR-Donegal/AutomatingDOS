# Finally

In this session you've learned how to do basic batch files at the command prompt. Some of you will consider this to be anachronistic and no longer of use. Unfortunately old technologies never go away!

You will come across the requirements to use the techniques demonstrated here in the rest of this module and in your future career.

For automation to work properly, it requires an attention to detail. In September 2024, I moved my coursework submission for this module to GITHUB. Students were instructed to:

* Create a GITHUB account with their L Number.
* Create repos with defined names for each submission.
* Invite the lecturer as a collaborator.

I exported a list of students taking this module and saved it as **LNumbers.txt**. For the coursework called "first", I created the following script; look through it, make sure you understand what I did.

```
:: Batch file to download student assignments 
:: By: JOR
:: Initial file: 09NOV24
:: Filename: first.cmd

@echo off
setlocal enabledelayedexpansion

:: Specify the text file to read
set "inputFile=../LNumbers.txt"

:: Check if the file exists
if not exist "%inputFile%" (
    echo File not found: %inputFile%
    exit /b
)

:: Read each line from the file
for /f "tokens=* delims=" %%A in (%inputFile%) do (
    git clone https://github.com/"%%A"/first
    ren first %%A
    echo %%A
)

endlocal
```

As long as students followed my instructions, I now have a copy of their coursework, which I can provide to the course board AND the external examiner.

I pop into each directory to grade and I can list all the remote branches and see the commits.

```
git branch -r
git log --oneline --decorate --all --author="L00xxxxxx" 
```

Now I can look around to see what has been done!
