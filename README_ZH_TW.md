# GUI-PalDefender-up <a href="https://www.buymeacoffee.com/tocsh" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy SH A Coffee" height="36" width="120"></a>
適用於Palserver-GUI中的Paldefender檔案更新

> [!WARNING]
>
> 此更新程式雖然已經做了基本的運作測試
> 
> 但也有可能發生意外的情況
> 
> 請務必在做任何檔案變更移動時
> 
> 備份伺服器的存檔
> 
> 以免發生意料之外的狀況
>

## 目錄
- [語言](#語言)
- [關於](#關於)
- [功能](#功能)
- [安裝](#安裝)
- [問題](#問題)
- [作者](#作者)

## 語言
[English](./README.md) | 繁體中文

## 關於
為了防止錯誤的更新而建立的更新程式，
<br>鎖定更新的資料夾，
<br>抓取最新的檔案並取代現有檔案。
<br>
<br>代碼是閉源的，我們沒有計劃發布它。
<br>
<br>可以在 [palserver-GUI Discord](https://discord.gg/UA24pctUYc) 找到我。
<br>
<br>此README適用版本：
<br>GUI PalDefender up v1.3.1
<br>

## 功能
- [x] 偵測路徑是否正確
- [x] 檢查版本是否最新
- [x] 下載最新版本檔案
- [x] 輸出工作日誌
- [x] 支援自選instances
- [x] 免進入GUI按更新
- [x] 一次更新多伺服器
- [x] 程式語言選擇
- [x] 輸出設定文件
- [x] 刪除舊版檔案
- [x] 強制更新檔案
- [x] 清除日誌
- [x] 清除GUI暫存
- [x] 公告項目
- [ ] 新版本提示
- [ ] ?????

## 安裝
   ```
   GUI PalDefender up.exe 介紹
   ├── 系統設定
   │   ├── 選擇 GUI 路徑
   │   ├── 選擇 instances 路徑
   │   └── 語言
   ├── 檢查更新
   ├── 關於此程式
   │   └── 版本、簡介及公告
   ├── 清除日誌
   ├── 清除 GUI 暫存
   └── 離開系統
   ```
<img src="https://github.com/1476523/GUI-PalDefender-up/blob/main/img/ZH_TW00.jpg" alt="主頁面" height="602" width="612"></a>
1. 在 [GUI-PalDefender-up](https://github.com/1476523/GUI-PalDefender-up/releases) 下載最新版本
2. 將程式放在任意地方
3. 執行 `GUI PalDefender up.exe` (首次執行會出現語言設定)
4. 左鍵點擊 檢查更新 即可更新(首次需要先前往系統設定完成路徑設定)
   ```
   系統設定說明
   選擇 GUI 路徑：
   請選擇啟動 palserver-gui 的捷徑或執行檔

   選擇 instances 路徑：
   請點擊 使用預設路徑 或選擇您自訂的路徑(通常是使用預設)

   設定完畢請按 保存設定
   否則設定將不會被儲存
   ```
   <img src="https://github.com/1476523/GUI-PalDefender-up/blob/main/img/ZH_TW01.jpg" alt="系統設定" height="602" width="612"></a><br>
5. 更新結果會顯示於 `GUI PalDefender up.exe` 下方(執行速度很快且通常是秒完成)。
6. 啟動伺服器後，
   <br>查看CMD上方的 `Starting PalDefender Anti Cheat` 是否已經是最新版本。

## 問題
1. 按下 Palguard 的更新後，PalDefender 沒有更新至最新版本。
   -  可能 PalDefender 尚未更新，
 <br> 請查看 [PalDefender](https://github.com/Ultimeit/PalDefender) 是否有版本更新。
   -  可能執行 GUI-PalDefender-up 時出現問題，
 <br> 請在更新後查看 `GUI PalDefender up.exe` 下方提示。
   -  可能未正常覆蓋 PalDefender 檔案(`包含Beta版`)，
 <br> 請對 `檢查更新` 按下 `滑鼠右鍵` 來進行 `強制更新檔案` 。

## 作者
- [GUI-PalDefender-up](https://github.com/1476523/GUI-PalDefender-up) [1476523](https://github.com/1476523)
- [PalDefender](https://github.com/Ultimeit/PalDefender) [Ultimeit](https://github.com/Ultimeit) [Zvendson](https://github.com/Zvendson)
- [palserver-GUI](https://github.com/Dalufishe/palserver-GUI) [Dalufishe](https://github.com/Dalufishe)


