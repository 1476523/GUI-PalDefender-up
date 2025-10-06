# GUI-PalDefender-up <a href="https://www.buymeacoffee.com/tocsh" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy SH A Coffee" height="36" width="120"></a>
Applicable to PalDefender archive updates within palserver-gui.

> [!WARNING]
>
> Although this update program has undergone basic operational testing,
> 
> But unexpected situations may occur.
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
<br>Lock the updated folder,
<br>Crawl the latest archives and replace the existing ones.
<br>
<br>The code is closed source and we dont have any plans to release it.
<br>
<br>I can be found in [palserver-GUI Discord](https://discord.gg/UA24pctUYc).
<br>
<br>This README is suitable for version：
<br>GUI PalDefender up v1.3
<br>

## Features
- [x] Check whether the file path is correct.
- [x] Check if the version is latest.
- [x] Download the latest version of the archive.
- [x] Output work log.
- [x] Supports optional instances.
- [x] No need to go to the server settings of the palserver-GUI to click Update.
- [x] Update multiple servers at once.
- [x] Tools language selection.
- [x] Output settings file.
- [x] Delete old file.
- [x] Forced update of files.
- [x] Clear log
- [x] Clear GUI Cache
- [ ] ?????

## Installation
   ```
   GUI PalDefender up.exe introduce
   ├── System Settings
   │   ├── Select GUI path
   │   ├── Select instances path
   │   └── Language
   ├── Check Updates
   ├── About This Program
   │   └── Version and introduction
   ├── Clear Log
   ├── Clear GUI Cache
   └── Exit
   ```
1. Download the latest release at [GUI-PalDefender-up](https://github.com/1476523/GUI-PalDefender-up/releases)
2. Put the program anywhere.
3. Execute `GUI PalDefender up.exe` (Language settings will appear for the first execution).
4. Click `Check Updates` to update (you need to go to `System Settings` for the first time to complete the path settings).
   ```
   System Setting Description
   Select GUI path：
   Please select palserver-gui's shortcut or execution file (that is, the file started by palserver-gui).

   Select instances path：
   Please click Use Default Path or select your customized path (usually using a preset)

   After the settings are completed, please press Save settings to save the settings.
   If you don't click on Save settings, the settings will not be stored.
   ```
5. The update results will be displayed below `GUI PalDefender up.exe` (execution is fast and usually completed in seconds).
6. After starting the server
   <br>Check whether the `Starting PalDefender Anti Cheat` displayed above `CMD` is already the latest version.

## Question
1. After pressing the update of Palguard, PalDefender has not been updated to the latest version.
   -  Maybe PalDefender has not been updated yet,
    <br> Please go to [PalDefender](https://github.com/Ultimeit/PalDefender) to see if there is a version update.
   -  There may be a problem in the GUI-PalDefender-up,
    <br> Please check the prompts below `GUI PalDefender up.exe` after the update.
   -  The PalDefender file may not be covered normally(`Including Beta version`),
    <br> Right-click `Check Updates` to force an update.

## Authors
- [GUI-PalDefender-up](https://github.com/1476523/GUI-PalDefender-up) [1476523](https://github.com/1476523)
- [PalDefender](https://github.com/Ultimeit/PalDefender) [Ultimeit](https://github.com/Ultimeit) [Zvendson](https://github.com/Zvendson)
- [palserver-GUI](https://github.com/Dalufishe/palserver-GUI) [Dalufishe](https://github.com/Dalufishe)
