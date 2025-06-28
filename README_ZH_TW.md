GUI-PalDefender-up
<br>適用於Palserver-GUI中的Paldefender檔案更新
<br>
[English](./README.md) | 繁體中文 |
<br>
> [!注意]
>
> 此更新程式雖然已經做了基本的運作測試，但也有可能發生意外的情況。
> 
> 請務必在做任何檔案變更移動時
> 
> 備份伺服器的存檔
> 
> 以免發生意料之外的狀況
>

## 目錄 (#目錄)
* [關於](#關於-)
* [功能](#功能-)
* [安裝](#安裝-)
* [問題](#問題-)
* [作者](#作者-)

## 關於 [↑](#GUI-PalDefender-up)

<br>為了防止錯誤的更新而建立的更新程式，
<br>鎖定更新的資料夾並備份原始檔案，
<br>抓取最新的檔案並取代現有檔案。
<br>
<br>代碼是閉源的，我們沒有計劃發布它。
<br>
<br>可以在 [palserver-GUI Discord](https://discord.gg/UA24pctUYc) 找到我。


<br>

## 功能 [↑](#目錄)

- [x] 偵測路徑是否正確
- [x] 備份現有版本檔案
- [x] 檢查版本是否最新
- [x] 下載最新版本檔案
- [x] 輸出工作日誌
- [] ????

<br>

## 安裝 [↑](#目錄)

1. 在 [github](https://github.com/1476523/GUI-PalDefender-up/releases) 下載最新版本
2. 將程式放在你的 `Palguard` 資料夾內
   <br>目錄結構應如下所示：
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
   │   │   │   │   ├── Palguard                    # << 放在此處
   │   │   │   │   │   ├── xxx/                    # << 將生成此文件夾
   │   │   │   │   │   ├── GUI PalDefender up.exe  # << 這個程式
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
3. 請先關閉 `palserver-gui` 後再啟動 `GUI PalDefender up.exe`，
4. 執行 `GUI PalDefender up.exe` 時將會備份原始檔案並檢查更新。
   <br>執行 `GUI PalDefender up.exe` 時將會執行以下步驟：
   ```
   GUI PalDefender up.exe 啟動
   └── 檢查目前檔案
       ├── 檔案存在
       │   └── 讀取版本號
	   │       └── 建立備份資料夾
	   │           └── 檢查更新
	   │               ├── 已經是最新版本
	   │               │   └── 建立或更新執行日誌
	   │               │       └── 完畢
	   │               └── 不是最新版本
	   │                   └── 下載最新檔案
	   │                       └── 建立或更新執行日誌
	   │                           └── 完畢
	   └── 檔案不存在
	       └── 下載最新檔案
		       └── 建立或更新執行日誌
			   	   └── 完畢
   ```
5. `GUI PalDefender up.exe` 執行速度很快(通常是秒完成)，
   <br>可以檢查執行日誌來確認更新是否成功。
6. 啟動伺服器後，
   <br>查看CMD上方的 `Starting PalDefender Anti Cheat` 是否已經是最新版本。
7. 當備份資料夾過多時，
   <br>為了安全起見，請保留最近2個版本的備份(含當前版本)。
   <br>檔案刪除的範例：
   ```
   Palguard
   ├── 140/                    # << 可以刪除的資料夾
   ├── 141/                    # << 可以刪除的資料夾
   ├── 142/                    # << 上一個版本的備份資料夾
   ├── 143/                    # << 目前版本的備份資料夾
   ├── GUI PalDefender up.exe
   ├── PalDefender.dll
   ├── palguard.version.txt    # << 在此可以查看目前版本號碼
   └── version.dll
   ```
<br>

## 問題 [↑](#目錄)

1. 按下 Palguard 的更新後，PalDefender 沒有更新至最新版本。
   -  可能 PalDefender 尚未更新，
 <br> 請查看執行日誌與 [PalDefender](https://github.com/Ultimeit/PalDefender) 。
   -  可能執行 GUI-PalDefender-up 時出現問題，
 <br> 請查看執行日誌。
   -  可能未正常覆蓋 PalDefender 檔案，
 <br> 請前往 palserver-GUI > 以滑鼠右鍵點擊伺服器 > 伺服器資料夾 > `Pal\Binaries\Win64`
 <br> 找到並刪除這三個檔案 `PalDefender.dll` `palguard.version.txt` `version.dll`
 <br> 前往 palserver-GUI > 伺服器設定 > Palguard 需要更新！ > 更新

<br>

## 作者 [↑](#目錄)

- [GUI-PalDefender-up](https://github.com/1476523/GUI-PalDefender-up) [1476523](https://github.com/1476523)
- [PalDefender](https://github.com/Ultimeit/PalDefender) [Ultimeit](https://github.com/Ultimeit) [Zvendson](https://github.com/Zvendson)
- [palserver-GUI](https://github.com/Dalufishe/palserver-GUI) [Dalufishe](https://github.com/Dalufishe)
