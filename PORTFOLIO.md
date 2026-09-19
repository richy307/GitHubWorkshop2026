![工作坊完成徽章](https://img.shields.io/badge/GitHub_Copilot_實戰工作坊-已完成-1F883D?style=for-the-badge&logo=githubcopilot&logoColor=white)

![Agent Mode](https://img.shields.io/badge/Agent_Mode-已實作-1E2761?style=flat-square)
![MCP](https://img.shields.io/badge/MCP-已整合-1E2761?style=flat-square)
![Agentic Workflow](https://img.shields.io/badge/Agentic_Workflow-已建立-1E2761?style=flat-square)

# 待辦清單 Web App

這是一個在 GitHub Copilot 實戰工作坊中完成的待辦清單 Web App。使用者可以新增、完成、篩選與整理待辦事項，資料會保存在瀏覽器中，方便在重新開啟頁面後繼續使用。

## 線上展示

[開啟 GitHub Pages](https://richy307.github.io/GitHubWorkshop2026/)

## 功能

- 新增待辦事項，並限制輸入長度。
- 勾選或取消勾選待辦事項，切換完成狀態。
- 刪除單筆待辦事項。
- 依照「全部」、「未完成」與「已完成」篩選待辦事項。
- 當目前篩選結果為空時，顯示對應的提示文字。
- 顯示目前未完成的待辦事項數量。
- 一次清除所有已完成事項，操作前使用瀏覽器內建確認對話框。
- 沒有已完成事項時停用「清除已完成」按鈕。
- 使用 `localStorage` 保存待辦事項與手動選擇的色彩主題。
- 支援淺色模式與深色模式，並可依照作業系統的 `prefers-color-scheme` 偏好自動套用。
- 提供基本的鍵盤與輔助技術支援，例如表單標籤、按鈕的 `aria-label` 與動態清單提示。
- 在小螢幕裝置上調整版面配置。

## 技術

- 使用純 HTML、CSS 與原生 JavaScript。
- 不使用任何前端框架或第三方套件。
- 不建立或依賴 `package.json`，也不需要執行 `npm install`。
- 不引用外部 CDN，專案可以離線運作。
- 使用瀏覽器原生 `localStorage` 保存待辦資料與主題偏好。
- 使用 CSS 自訂變數集中管理色彩，並透過 CSS media query 支援深色模式。

## 開發方式

這個專案在 GitHub Copilot 實戰工作坊中，透過以下方式逐步完成：

- **GitHub Copilot Agent Mode**：以自然語言描述需求，協助建立待辦清單介面與互動功能，並依照 issue 需求進行功能修正。
- **MCP**：透過 GitHub MCP 讀取 repository issue、確認需求與建立 Pull Request；也使用 Microsoft Learn MCP 查詢 `prefers-color-scheme` 與網頁色彩對比的官方文件，作為深色模式檢查的參考。
- **`.github/prompts` 的 agentic workflow**：使用 `fix-issue.prompt.md` 定義處理 issue 的工作流程，依序讀取 issue、提出計畫等待確認、建立修復分支、修改必要檔案、驗證、提交推送，以及建立 Pull Request。

## 我學到什麼

- 如何使用 GitHub Copilot Agent Mode，將需求逐步轉換成可操作的前端功能。
- 如何透過 MCP 連接 GitHub 與 Microsoft Learn 等工具，取得 issue 與官方技術文件資訊。
- 如何用 `.github/prompts` 建立具有明確步驟與確認點的 agentic workflow。
- 如何使用 `localStorage` 保存瀏覽器端資料，並在資料變更後同步更新畫面。
- 如何從使用者情境檢查篩選、確認對話框、色彩主題與基本無障礙需求。
