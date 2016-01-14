# GameDev: Mounting your home directory

Description

  - Open Notepad
  - Copy and Paste the setup code
  - Save as .bat file

### Setup

# 1. Copy the following  code:
```sh
@echo off

REM Drive mapping script for GameDev students in AOIT Lab
REM at Balboa High School

set NASHOST=10.64.11.25

echo MOUNTING HOME DIRECTORY FOR USER %USERNAME%

if exist w: net use w: /delete
net use w: \\%NASHOST%\%USERNAME%

if exist w: explorer w:
if not exist w: goto ERROR
exit

:ERROR
echo THERE HAS BEEN A PROBLEM MOUNTING \\10.64.11.25\%USERNAME%
pause

```

# 2. Open and paste to Notepad

Start>Notepad

* Dropbox
* Github
* Google Drive
* OneDrive

# 2. Save File as .bat 
Readmes, how to use them in your own application can be found here:

* [plugins/dropbox/README.md] [PlDb]
* [plugins/github/README.md] [PlGh]
* [plugins/googledrive/README.md] [PlGd]
* [plugins/onedrive/README.md] [PlOd]
