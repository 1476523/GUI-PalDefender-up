## GUI-PalDefender-up
Applicable to PalDefender archive updates within palserver-gui.
<br>
<br>
English | [繁體中文](./README_ZH_TW.md)

> [!WARNING]
>
> Although this update program has undergone basic operational testing,unexpected situations may occur.
> 
> Be sure to make any file changes or file movements,
> 
> Backup the server archive,
> 
> Avoid unexpected situations。
>

## Table of Contents
* [About](#about-)
* [Features](#features-)
* [Installation](#installation-)
* [Question](#Question-)
* [Authors](#authors-)

## About []()

This program is to prevent incorrect updates,
<br>Lock the updated folder and back up the original archive,
<br>Crawl the latest archives and replace the existing ones.
<br>
<br>The code is closed source and we dont have any plans to release it.
<br>
<br>I can be found in [palserver-GUI Discord](https://discord.gg/UA24pctUYc).

## Features []()

- [x] Check whether the file path is correct.
- [x] Back up existing version archives.
- [x] Check if the version is latest.
- [x] Download the latest version of the archive.
- [x] Output work log.
- [] ????

<br>

## Installation []()

1. Download the latest release at [GUI-PalDefender-up](https://github.com/1476523/GUI-PalDefender-up/releases)
2. Place the file in your `Palguard` folder.
   <br>It should look like this：
   ```
   palserver-gui/
   ├── locales/
   ├── resources/
   │   ├── app/
   │   ├── assets/
   │   │   ├── engine/
   │   │   │   ├── server-icons/
   │   │   │   ├── server-online-map/
   │   │   │   ├── server-template/
   │   │   │   │   ├── Config
   │   │   │   │   ├── Palguard                    # << Put here
   │   │   │   │   │   ├── xxx/                    # << Will be generated
   │   │   │   │   │   ├── GUI PalDefender up.exe  # << This program
   │   │   │   │   │   ├── PalDefender.dll
   │   │   │   │   │   ├── palguard.version.txt
   │   │   │   │   │   └── version.dll
   │   │   │   │   ├── Saved
   │   │   │   │   └── UE4SS
   │   │   │   ├── steamcmd-engine/
   │   │   │   └── engine.config.json
   │   │   ├── game-data/
   │   │   ├── icons/
   │   │   ├── <...>
   │   │   ├── icon.png
   │   │   └── icon.svg
   │   ├── app-update.yml
   │   └── elevate.exe
   ├── <...>
   ├── LICENSE.electron.txt
   ├── LICENSES.chromium.html
   ├── palserver-gui.exe
   └── <...>
   ```
3. Please close `palserver-gui` first before starting `GUI PalDefender up.exe`.
4. When `gui paldefender up.exe` is executed, the original archive will be backed up and the online archive will be checked for updates.
   <br>The following steps will be performed when executing `GUI PalDefender up.exe`:
   ```
   GUI PalDefender up.exe Start
   └── Check current files
       ├── Archives exist
       │   └── Read version number
	   │       └── Create a backup folder
	   │           └── Check for updates
	   │               ├── It's already the latest version
	   │               │   └── Create or update execution log
	   │               │       └── complete
	   │               └── Not the latest version
	   │                   └── Download the latest archives
	   │                       └── Create or update execution log
	   │                           └── complete
	   └── The file does not exist
	       └── Download the latest archives
		       └── Create or update execution log
			   	   └── complete
   ```
5. `GUI PalDefender up.exe` executes very fast (usually completed in seconds),
   <br>You can check the execution log to confirm that the update is successful.
6. After starting the server,
   <br>Check if Starting PalDefender Anti Cheat above CMD is already the latest version.
7. When there are too many backup folders,
   <br>For security reasons, please keep the backup of the last 2 versions (including the current version).
   <br>Example of folder deletion：
   ```
   Palguard
   ├── 140/                    # << File folders that can be deleted
   ├── 141/                    # << File folders that can be deleted
   ├── 142/                    # << The backup folder of the previous version
   ├── 143/                    # << The backup folder for the current version
   ├── GUI PalDefender up.exe
   ├── PalDefender.dll
   ├── palguard.version.txt    # << You can view the current version number here
   └── version.dll
   ```
<br>

## Question []()

1. After pressing the update of Palguard, PalDefender has not been updated to the latest version.
   -  Maybe PalDefender has not been updated yet,
    <br> Please check the execution log and [PalDefender](https://github.com/Ultimeit/PalDefender) .
   -  There may be a problem in the GUI-PalDefender-up,
    <br> Please check the execution log.
   -  The PalDefender file may not be covered normally,
    <br> Please go to palserver-GUI > Right-click the server > Server Folder > `Pal\Binaries\Win64`,
    <br> Find and delete these three files `PalDefender.dll` `palguard.version.txt` `version.dll`,
    <br> Please go to palserver-GUI > Server Settings > Palguard Needs Upgrade! > Upgrade > Finish.

<br>

## Authors []()

- [GUI-PalDefender-up](https://github.com/1476523/GUI-PalDefender-up) [1476523](https://github.com/1476523)
- [PalDefender](https://github.com/Ultimeit/PalDefender) [Ultimeit](https://github.com/Ultimeit) [Zvendson](https://github.com/Zvendson)
- [palserver-GUI](https://github.com/Dalufishe/palserver-GUI) [Dalufishe](https://github.com/Dalufishe)
