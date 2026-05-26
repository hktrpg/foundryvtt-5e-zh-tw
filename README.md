# 龍與地下城五版（DnD 5e）正體中文翻譯

[![Foundry VTT v10+](https://img.shields.io/badge/Foundry%20VTT-v10%2B-blue)](https://foundryvtt.com/)
[![D&D 5e System](https://img.shields.io/badge/D%26D%205e-3.x-orange)](https://github.com/foundryvtt/dnd5e)
[![總下載次數](https://img.shields.io/github/downloads/hktrpg/foundryvtt-5e-zh-tw/total?label=%E7%B8%BD%E4%B8%8B%E8%BC%89%E6%AC%A1%E6%95%B8)](https://github.com/hktrpg/foundryvtt-5e-zh-tw/releases)

這是 [D&D 5th Edition](https://github.com/foundryvtt/dnd5e) 系統在 Foundry VTT 上的**正體中文**在地化模組。

## 來源與轉換說明

本模組主要參考以下專案的簡體中文翻譯：

- **原始簡體中文來源**： [fvtt-cn/5e_chn](https://github.com/fvtt-cn/5e_chn)

本專案使用 **ConvertZZ**（轉換精靈）工具，將簡體中文版本轉換為**正體中文（台灣用語）**，並針對常見遊戲術語進行人工校對調整。

### 維護流程（供貢獻者參考）

1. 從 [fvtt-cn/5e_chn](https://github.com/fvtt-cn/5e_chn) 取得最新版本的簡體中文翻譯檔。
2. 使用 **ConvertZZ** 進行簡繁轉換。
3. 將轉換後的內容更新至 `lang/zh-tw.json`。
4. 來源檔案會保留在 `source/` 目錄中，方便比對版本差異。

## 安裝方式

### 推薦安裝方式（模組管理器）

1. 開啟 Foundry VTT → 點擊「模組管理」（Module Management）。
2. 點擊右上角「安裝模組」（Install Module）。
3. 直接輸入以下 Manifest 網址：
   ```
   https://raw.githubusercontent.com/hktrpg/foundryvtt-5e-zh-tw/refs/heads/main/module.json
   ```
4. 安裝完成後，在模組列表中啟用本模組。

### 手動安裝

1. 從 [Releases](https://github.com/hktrpg/foundryvtt-5e-zh-tw/releases) 下載最新版本的 `module.zip`。
2. 解壓縮到 Foundry VTT 的模組資料夾：
   ```
   FoundryVTT/Data/modules/dnd5e-cn-2-zh-tw/
   ```
3. 在遊戲設定中啟用模組。

## 使用方式

1. 安裝並啟用本模組。
2. 進入「遊戲設定」→「核心設定」，將「語言」切換為 **正體中文**。
3. 重新載入世界（Reload World）即可看到完整正體中文介面。

> **注意**：本模組僅提供翻譯功能，不包含規則內容。請務必同時安裝官方的 `dnd5e` 系統。

## 相容性

- **Foundry VTT**：v10 以上（已驗證至 v12）
- **D&D 5e 系統**：2.2.0 以上（已驗證至 3.3.0）

## 貢獻

歡迎任何翻譯修正、建議或 Pull Request！

- 原始簡體中文專案：[fvtt-cn/5e_chn](https://github.com/fvtt-cn/5e_chn)
- 本專案 GitHub：[hktrpg/foundryvtt-5e-zh-tw](https://github.com/hktrpg/foundryvtt-5e-zh-tw)

如發現翻譯問題或有更好的用語建議，請到 GitHub 開 Issue 討論。

## 致謝

- 感謝 [fvtt-cn](https://github.com/fvtt-cn) 團隊提供高品質的簡體中文翻譯基礎。
- 感謝 HKTRPG 社群協助維護與轉換工作。
- 感謝所有參與校對與提供意見的玩家們。

## 授權

本模組遵循原始專案的授權方式發布。

## 發布新版本（自動打包）

本專案使用 GitHub Actions 自動根據 `module.json` 中的版本號打包發布。

### 發布步驟

1. 修改 `module.json` 中的 `version` 欄位（例如 `1.5.3.3.1`）
2. 提交變更並推送：
   ```bash
   git add module.json
   git commit -m "chore: bump version to 1.5.3.3.1"
   git push
   ```
3. 建立與版本號相同的 tag 並推送：
   ```bash
   git tag 1.5.3.3.1
   git push origin 1.5.3.3.1
   ```
4. GitHub Actions 會自動執行：
   - 讀取 `module.json` 的版本號
   - 只打包 `lang/`、`module.json`、`README.md` 成 `module.zip`
   - 建立 Release 並上傳 `module.zip`

發布完成後，使用者即可透過以下網址取得最新版本：
```
https://github.com/hktrpg/foundryvtt-5e-zh-tw/releases/latest/download/module.zip
```

你也可以在 GitHub 頁面 → Actions → "Release Foundry Module" → 手動觸發（workflow_dispatch）來測試打包流程。

---

如果這個模組對你有幫助，歡迎給個 Star 支持一下！
