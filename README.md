## EDC MasterHook

emuDownloadCenter (EDC) is a program to download ROM emulators from internet.
Mostly in depots where found emulators on the internet are stored.
Author: Sebastiaan Ebeltjes, Deventer (Netherlands)

EDC is part of [**emuControlCenter**](https://github.com/PhoenixInteractiveNL/emuControlCenter/wiki)

### [**Browse emulators**](https://github.com/PhoenixInteractiveNL/edc-masterhook/tree/master/downloadhooks#emulator-listing)
***
## Your help

Want to help us expanding EDC emulators?, please install [**GitHub Desktop**](https://desktop.github.com)

Fork this repo (edc-masterhook)

Fork the latest [edc-repo00??](https://github.com/PhoenixInteractiveNL)

and make pull requests!
***
Some site's to get emulators:

http://www.emulator-zone.com

http://www.zophar.net

https://www.aep-emu.de

http://www.emu-france.com

***
## Emulatorlist.ini

To prevent folder names with spaces and give nice emulator names in EDC listings, this ini wil link those names.

**INI SECTION = ECCID**

Format: `FOLDER=EMULATORNAME`
***
## Emulator Hooks

Every emulator (not versions) are put in a `downloadhooks\[emulatorfoldername]` folder, in here 3 files are stored:

2 INI files wich contain data

1 JPG file wich is a screenshot of the emulator (in action)

    [emulatorfoldername]_downloads.ini
    [emulatorfoldername]_info.ini
    [emulatorfoldername]_screen

**Please note: all in lowercase names!**
***
## Emulator INFO INI

Example Contents (Emulator Potator for Watara Supervision):

    [INFO]
    InfoVersion         = 1.0.0.0

    [EMULATOR]
    Author              = David Raingeard
    Contact             = david*raingeard#laposte*net
    License             = Freeware
    BiosNeeded          = 0
    Website             = 
    Notes               = This appears to be the first Watara Supervision emulator for Windows. It uses the SDL library and has good compatibility.

Please note the Email is masked to prevent spamming (*=. | #=@)

**Info breakdown:**

    [INFO]
    InfoVersion	        = Version of the INI file layout.

    [EMULATOR]
    Author              = Author of the emulator.
    Contact             = Possible E-mail of the Author.
    License             = The License of the Emulator (Freeware/Shareware/Open Source/GPL).
    BiosNeeded          = Does the Emulator need BIOS ROMS to run?
    Website             = Website where the emulator can be found.
    Notes               = Small description of the emulator.

***
## Emulator DOWNLOADS INI

**INI SECTION = VERSION**

**EMU** contents are EMULATOR relative.

**CFG** contents are ECC relative.

**INFO** contents are FILE relative, and are generated by the EDC manager (you may fill these yourself)

Example Contents (Emulator Potator for Watara Supervision):

    [0.7]
    EMU_Download                = https://github.com/PhoenixInteractiveNL/edc-repo0001/raw/master/potator/
    EMU_ReleaseDate             = 2004-10-19
    EMU_Notes                   = Has a commandline parameter to start roms.
    EMU_ExecutableFile          = Potator.exe
    EMU_ExecutableFolder        =
    EMU_OS                      = Windows
    EMU_OSVersion               = XP,Vista,7,8,10
    EMU_OSArchitecture          = x86,x64
    CFG_ECCParameter            = %ROM%
    CFG_escape                  = 1
    CFG_win8char                =
    CFG_useCueFile              =
    CFG_filenameOnly            =
    CFG_noExtension             =
    CFG_executeInEmuFolder      =
    CFG_enableEccScript         = 
    CFG_enableZipUnpackActive   =
    CFG_enableZipUnpackSkip     =
    INFO_PackedSize             = 179 
    INFO_UnpackedSize           = 192 
    INFO_CRC32Executable        = 6C059FFB 
    INFO_CRC32Archive           = A8E52604

**Info breakdown:**

    [0.7]
    EMU_Download                = The online location of the 7Z archive file (with ending slash /)
    EMU_ReleaseDate             = The releasedate of the emulator (if you cannot find it, use the date on the executable file)
    EMU_Notes                   = Some small emulator notes (Working / Not working)
    EMU_ExecutableFile          = Executable file to start the emulator (EXE/COM), please no CMD/BAT files.
    EMU_ExecutableFolder        = Path inside archive where executable file is located.
    EMU_OS                      = Operating system.
    EMU_OSVersion               = Version of the operating system, comma seperated. (example: XP,Vista,7,8,10)
    EMU_OSArchitecture          = Operating system architecture, comma seperated. (example: x86,x64)
    CFG_ECCParameter            = ECC parameter line.
    CFG_escape                  = Does the emulator needs the path in escapes? "" (default 1)
    CFG_win8char                = Does the emulator need old 8.3 dosnames to work? (1 for yes, otherwise leave blank)
    CFG_useCueFile              = Does the emulator needs a CUE file (possible in combination with script) to run? (1 for yes, otherwise leave blank)
    CFG_filenameOnly            = Does the emulator only needs the filename to run? (1 for yes, otherwise leave blank)
    CFG_noExtension             = Does the emulator only needs the filename to run without extension? (1 for yes, otherwise leave blank)
    CFG_executeInEmuFolder      = Does the emulator needs to be executed from withing the emulator folder? (1 for yes, otherwise leave blank)
    CFG_enableEccScript         = Does the emulator need a ECC script to start and run a ROM? (1 for yes, otherwise leave blank)
    CFG_enableZipUnpackActive   = Does the ROM archive need to be extracted first? (1 for yes, otherwise leave blank)
    CFG_enableZipUnpackSkip     = Skip already unpacked files (faster). (1 for yes, otherwise leave blank)
    INFO_PackedSize             = Packed size of the archive contents.
    INFO_UnpackedSize           = Unpacked size of the archive contents.
    INFO_CRC32Executable        = CRC32 of the executable to start the emulator.
    INFO_CRC32Archive           = CRC32 of the emulator archive.
***
## The download folder

Every emulator version needs 3 files:

    [version].7z
    [version]_changelog.txt
    [version]_contents.txt

### Changelog
The changelog for this version, you may need to search for it on the emulator website, or any readme document in the archive...

Note that if there are more builds of the same version, then just copy the changelog, example:

1.0-win32_changelog.txt
1.0-win64_changelog.txt (same contents as above)

### Contents
Archive contents (will be created by EDC manager)

***
Please leave these emulators out for now:

- Emulators for **Linux** and **MacOs** (you can add them to the repo, don't add them in downloads.ini)
- Emulators **Source** files (you can add them to the repom, don't add them in downloads.ini)
- Emulators that have **installers** to run first.
- Emulators that are **Java** based (JAR).
