# flowmoor

<div align="center">

![flowmoor](public/icon.png)

**現代化的 Twitch 與 YouTube 影片下載器**

[![Version](https://img.shields.io/badge/version-2.1.0-blue.svg)](https://github.com/EsabiyaXCF/flowmoor)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Electron](https://img.shields.io/badge/Electron-27.0.0-9feaf9.svg)](https://www.electronjs.org/)
[![React](https://img.shields.io/badge/React-18.2.0-61dafb.svg)](https://reactjs.org/)

[功能特色](#功能特色) • [安裝說明](#安裝說明) • [使用方法](#使用方法) • [開發指南](#開發指南) • [常見問題](#常見問題)

</div>

## 📖 專案簡介

flowmoor 是一個基於 Electron 和 React 開發的現代化影片下載器，支援從 YouTube 和 Twitch 平台下載高品質影片。採用繁體中文介面設計，提供直觀易用的操作體驗。

## ✨ 功能特色

### 🎯 核心功能
- **多平台支援** - 支援 YouTube 和 Twitch VOD 下載
- **自動品質檢測** - 智慧識別並提供所有可用的影片品質選項
- **部分下載** - 支援指定時間範圍下載影片片段
- **批次下載** - 同時管理多個下載任務
- **進度追蹤** - 即時顯示下載進度、速度和剩餘時間

### 🎨 使用者介面
- **現代化設計** - 採用 Material Design 風格的深色主題
- **流暢動畫** - 使用 Framer Motion 提供順滑的介面動畫
- **響應式佈局** - 支援不同視窗大小的自適應佈局
- **繁體中文** - 完整的繁體中文本地化支援

### 🛠 進階功能
- **下載管理** - 暫停、恢復、取消下載任務
- **歷史記錄** - 完整的下載歷史和狀態追蹤
- **自訂設定** - 可配置下載路徑、品質偏好等設定
- **OAuth 支援** - 支援 Twitch OAuth 下載私人內容
- **自動更新** - 自動檢查並更新 yt-dlp 等核心組件

## 🚀 安裝說明

### 系統需求
- **作業系統**: Windows 10/11 (64-bit)
- **記憶體**: 至少 4GB RAM
- **硬碟空間**: 至少 500MB 可用空間
- **網路連線**: 穩定的網際網路連線

### 預構建版本安裝

1. 前往 [Releases](https://github.com/yourusername/flowmoor/releases) 頁面
2. 下載最新版本的 `flowmoor Setup 2.1.0.exe`
3. 執行安裝檔案並按照指示完成安裝
4. 首次啟動時會自動下載必要的依賴組件

## 📱 使用方法

### 基本下載流程

1. **啟動應用程式**
   - 點擊桌面圖示或從開始選單啟動

2. **輸入影片連結**
   - 在 URL 輸入框中貼上 YouTube 或 Twitch 影片連結
   - 支援的格式：
     - YouTube: `https://www.youtube.com/watch?v=...`
     - Twitch VOD: `https://www.twitch.tv/videos/...`

3. **抓取影片資訊**
   - 點擊「貼上並抓取」按鈕或按 Enter 鍵
   - 等待系統分析影片並顯示詳細資訊

4. **配置下載設定**
   - **影片品質**: 選擇所需的影片解析度和品質
   - **檔案名稱**: 自訂輸出檔案的名稱
   - **時間範圍**: 可選擇下載特定時間段
   - **輸出路徑**: 選擇檔案儲存位置

5. **開始下載**
   - 點擊「開始下載」按鈕
   - 在進度列表中即時監控下載狀態

### 進階操作

#### 下載管理
- **暫停下載**: 點擊暫停按鈕暫時停止下載
- **恢復下載**: 點擊播放按鈕繼續暫停的下載
- **取消下載**: 點擊 X 按鈕完全取消下載任務

#### 歷史記錄
- 切換到「歷史」標籤查看所有下載記錄
- 點擊資料夾圖示快速開啟檔案位置
- 使用清除按鈕管理歷史記錄

#### 設定調整
- 點擊設定按鈕開啟設定對話框
- 可配置：預設下載路徑、品質偏好、主題風格等

## 🔧 設定說明

### 應用程式設定
- **下載路徑**: 預設使用系統下載資料夾，可自訂
- **影片品質**: 可設定預設的品質偏好 (best/worst/specific)
- **同時下載數**: 控制同時進行的下載任務數量 (預設: 3)
- **自動重試**: 啟用失敗後自動重試功能
- **通知**: 下載完成後顯示系統通知

### Twitch OAuth 設定
1. 前往 [Twitch Developers Console](https://dev.twitch.tv/console)
2. 建立新的應用程式並取得 OAuth Token
3. 在設定中輸入 OAuth Token 以存取私人內容

## 🐛 常見問題

### Q: 下載失敗顯示「yt-dlp 未找到」
**A**: 首次啟動時應用程式會自動下載 yt-dlp。如果失敗，請：
1. 檢查網路連線
2. 關閉防毒軟體暫時阻擋
3. 以管理員身份重新啟動應用程式

### Q: 無法下載某些 YouTube 影片
**A**: 可能原因：
- 影片有地區限制
- 影片為即時串流
- YouTube 更新了防護機制，需要更新 yt-dlp

### Q: Twitch VOD 下載失敗
**A**: 請確認：
- VOD 仍然可用（未被刪除）
- 如果是訂閱者專屬內容，需要設定 OAuth Token
- 檢查網路連線穩定性

### Q: 應用程式啟動緩慢
**A**: 首次啟動需要初始化各種組件，後續啟動會更快。如果持續緩慢：
1. 檢查系統資源使用情況
2. 確保有足夠的硬碟空間
3. 重新安裝應用程式

## 🤝 貢獻指南

歡迎提交 Issue 請確保：

1. **Issue**: 詳細描述問題和重現步驟

## 🆘 技術支援

- **問題回報**: [GitHub Issues](https://github.com/yourusername/flowmoor/issues)
- **功能建議**: [GitHub Discussions](https://github.com/yourusername/flowmoor/discussions)
- **聯絡方式**: your.email@example.com

## 📝 更新日誌

### v2.1.0 (2024-XX-XX)
- ✨ 新增 YouTube 影片下載支援
- 🎨 全新的統一下載介面設計
- 🚀 改善下載效能和穩定性
- 🌍 完整繁體中文本地化
- 🔧 增強的設定選項和 OAuth 支援

### v2.0.0 (2024-XX-XX)
- 🎉 首次正式發布
- 📱 現代化使用者介面
- 🎬 Twitch VOD 下載功能
- 📊 即時進度追蹤
- 📚 下載歷史管理

---

<div align="center">

**如果這個專案對您有幫助，請考慮給個 ⭐ Star！**

Made with ❤️ by [EsabiyaXCF](https://github.com/EsabiyaXCF)

</div>
