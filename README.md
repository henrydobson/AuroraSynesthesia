# AuroraSynesthesia
This is the new home for the screen and audio capture utility for controlling amBX lights, created by Christopher "ZodiusInfuser" Parrott.

This work is licensed under a Creative Commons Attribution-NonCommercial 4.0 International License.

## Windows 10

### The issue
The problem was that the lights would react to the screen but with a 3 second delay. After noticing that the project at https://github.com/ZodiusInfuser/AuroraSynesthesia was not running efficiently on Windows 10 and noting the pull request from https://github.com/entdark/AuroraSynesthesia, I decided to see if I could use this to improve the reactiveness for Cyborg amBX Gaming Lights.

Toolchain:
- Visual Studio 15
- [FMOD Studio Programmer’s API and Low Level Programmer API](http://www.fmod.org/download/fmodstudio/api/Win/fmodstudioapi10814win-installer.exe) from http://www.fmod.org/download/
- [amBX SDK](http://ambx.exsanio.de/amBX%20SDK%20(February%202009).exe) from http://ambx.exsanio.de/

Assistive guides:
- [Cuboid Zone](https://cuboidzone.wordpress.com/2013/07/26/tutorial-implementing-fmod/)
- [FMOD API Ref](http://www.fmod.org/documentation/#content/generated/lowlevel_api.html)
- [cannot open afxres.h](http://stackoverflow.com/questions/3566018/cannot-open-include-file-afxres-h-in-vc2010-express)
- [cannot open fmod_vc.dll](http://stackoverflow.com/questions/133698/why-does-fatal-error-lnk1104-cannot-open-file-c-program-obj-occur-when-i-c)
- [cannot open fmod_vc.dll]()

### The result
A working exe and reactive Cyborg amBX Gaming Lights! Bring on Alien Isolation!

### Notes
This was my first dive into C++ and Visual Studio and creating anything for Windows. It works but it's probably very buggy. If someone who knows what they are doing wants to clean it up, I'd welcome them too!

Known issues:
- I was unable to resolve an issue with the FMOD API. getSpectrum is no longer part of Channel and I don't know what would replace it. As I am not interested in the sound features of this app I simply commented this line out to build.
