# GUI-PalDefender-up
Applicable to PalDefender archive updates within palserver-gui.

> [!WARNING]
>
> Although this update program has undergone basic operational testing,unexpected situations may occur.
> 
> Be sure to make any file changes or file movements,
> 
> Backup the server archive,
> 
> Avoid unexpected situations.
>

## Table of Contents
- [language](#language)
- [About](#about)
- [Features](#features)
- [Installation](#installation)
- [Question](#question)
- [Authors](#authors)

## language
English | [繁體中文](./README_ZH_TW.md)

## About
This program is to prevent incorrect updates,
<br>Lock the updated folder and back up the original archive,
<br>Crawl the latest archives and replace the existing ones.
<br>
<br>The code is closed source and we dont have any plans to release it.
<br>
<br>I can be found in [palserver-GUI Discord](https://discord.gg/UA24pctUYc).
<br>
<br>This README is suitable for version：
<br>GUI PalDefender up v1.2
<br>

## Features
- [x] Check whether the file path is correct.
- [x] Back up existing version archives.
- [x] Check if the version is latest.
- [x] Download the latest version of the archive.
- [x] Output work log.
- [x] Supports optional instances.
- [x] No need to go to the server settings of the palserver-GUI to click Update.
- [x] Update multiple servers at once.
- [x] Tools language selection
- [x] Select GUI installation method
- [x] Output settings file
- [ ] ?????

## Installation
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
   │   │   │   │   ├── Palguard                           # << Put here
   │   │   │   │   │   ├── xxx/                           # << Will be generated
   │   │   │   │   │   ├── GUI PalDefender up config.ini  # << This file will be generated
   │   │   │   │   │   ├── GUI PalDefender up record.log  # << This file will be generated
   │   │   │   │   │   ├── GUI PalDefender up.exe         # << This program
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
   └── Check the settings file (GUI PalDefender up config.ini)
       ├── No files
       │   └── Display settings window
       │       └── Complete the settings
       │           └── Generate file GUI PalDefender up config.ini
       └── Have files
           └── Check the file path (GUI PalDefender up.exe placement path)
               ├── Wrong file path
               │   ├── Display error window
               │   └── Generate file GUI PalDefender up record.log
               └── Correct file path
                   └── Check current files
                       ├── The file does not exist
                       │   ├── Generate file GUI PalDefender up record.log
                       │   ├── Download the file PalDefender.dll
                       │   ├── Generate file palguard.version.txt
                       │   ├── Download the file version.dll
                       │   └── Show update prompt window
                       └── files exist
                           └── Generate folder with name of version number
                               ├── Backup files (Backup PalDefender.dll,version.dll,palguard.version.txt to this folder)
                               └── Check file version
                                   ├── Discover a new version
                                   │   └── Download the new version file
                                   └── No new version
                                       ├── Generate and write files GUI PalDefender up record.log
                                       └── Show update prompt window
                                           └── Check the instances folder of the server archive
                                               ├── The folder does not exist
                                               │   └── Display error window
                                               │       ├── Write to a file GUI PalDefender up record.log
                                               │       └── Open instances folder by user
                                               │           ├── Check as an error folder or not selected folder
                                               │           │   ├── Write to a file GUI PalDefender up record.log
                                               │           │   └── Terminate the program
                                               │           └── Check for the correct file folder
                                               │               ├── Write to a file GUI PalDefender up config.ini
                                               │               └── Write to a file GUI PalDefender up record.log
                                               └── The folder exists or the folder path has been set
                                                   └── Update folder files
                                                       └── Show update prompt window
                                                           └── Finish
   ```
5. `GUI PalDefender up.exe` executes very fast (usually completed in seconds),
   <br>You can check the `GUI PalDefender up record.log` to confirm that the update is successful.
6. After starting the server,
   <br>Check if Starting PalDefender Anti Cheat above CMD is already the latest version.
7. When there are too many backup folders,
   <br>For security reasons, please keep the backup of the last 2 versions (including the current version).
   <br>Example of folder deletion：
   ```
   Palguard
   ├── 142/                           # << File folders that can be deleted
   ├── 143/                           # << File folders that can be deleted
   ├── 144/                           # << The backup folder of the previous version
   ├── 145/                           # << The backup folder for the current version
   ├── GUI PalDefender up config.ini
   ├── GUI PalDefender up record.log
   ├── GUI PalDefender up.exe
   ├── PalDefender.dll
   ├── palguard.version.txt           # << You can view the current version number here
   └── version.dll
   ```

## Question
1. After pressing the update of Palguard, PalDefender has not been updated to the latest version.
   -  Maybe PalDefender has not been updated yet,
    <br> Please check the `GUI PalDefender up record.log` and [PalDefender](https://github.com/Ultimeit/PalDefender) .
   -  There may be a problem in the GUI-PalDefender-up,
    <br> Please check the `GUI PalDefender up record.log`.
   -  The PalDefender file may not be covered normally,
    <br> Please go to palserver-GUI > Right-click the server > Server Folder > `Pal\Binaries\Win64`,
    <br> Find and delete these three files `PalDefender.dll` `palguard.version.txt` `version.dll`,
    <br> Please go to palserver-GUI > Server Settings > Palguard Needs Upgrade! > Upgrade > Finish.

## Authors
- [GUI-PalDefender-up](https://github.com/1476523/GUI-PalDefender-up) [1476523](https://github.com/1476523)
- [PalDefender](https://github.com/Ultimeit/PalDefender) [Ultimeit](https://github.com/Ultimeit) [Zvendson](https://github.com/Zvendson)
- [palserver-GUI](https://github.com/Dalufishe/palserver-GUI) [Dalufishe](https://github.com/Dalufishe)
