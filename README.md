# RUSB
Ransomware on USB PoC using batch and aescrypt only

## Disclaimer
RUSB is purely academic, use at your own risk. I do not encourage in any way the use of this software illegally or to attack targets without their previous authorization.

## How it works

```
(R:)USB
 ├ Filename.txt.lnk
 └ System Volume Information
    ├ RUSB1.bat
    ├ RUSB2.bat
    ├ Aescrypt.exe
    └ Filename.txt
 ```
The folder `System Volume Information (SVI)` is automatically created by Windows for every partition, the main reason of us using it is that it cannot be seen by a regular user, even if the `see hidden files` option is enabled.

The whole process is simple:
The victim opens `Filename.txt.lnk` wich will open `RUSB1.bat`, `RUSB1.bat` will send `RUSB2.bat` and `Aescrypt.exe` (CLI) to `%USERPROFILE%` this files will encrypt all the user files, then create a file called `README.txt` at the desktop with the intructions to recover the files, after that they will encrypt theirselves.


#### This project is still in development
