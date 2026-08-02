# 《與 AI 同行》Quarto 部落格骨架

這是一個可直接使用的 Quarto 網站專案。照以下步驟，約 20 分鐘可上線。

## 一、安裝（只需一次）

1. 安裝 Quarto：到 <https://quarto.org/docs/get-started/> 下載 Windows 安裝檔，一路下一步。
2. 安裝 Git：<https://git-scm.com/downloads>（若已有可跳過）。
3. 確認安裝成功：開啟「命令提示字元」或 PowerShell，輸入：

   ```
   quarto check
   ```

## 二、本機預覽

在本資料夾（`ai-blog`）開啟終端機，執行：

```
quarto preview
```

瀏覽器會自動打開網站；您在 Typora 或任何編輯器改檔存檔，頁面會即時更新。

## 三、發佈到 GitHub Pages

1. 在 GitHub 建一個新 repo（例如 `ai-blog`，Public）。
2. 在本資料夾執行（`USERNAME` 換成您的帳號）：

   ```
   git init
   git add .
   git commit -m "init"
   git branch -M main
   git remote add origin https://github.com/USERNAME/ai-blog.git
   git push -u origin main
   quarto publish gh-pages
   ```

3. 第一次 `quarto publish gh-pages` 會問是否建立 gh-pages 分支，回答 Y。
   完成後網址是 `https://USERNAME.github.io/ai-blog/`。
4. 之後每次更新文章，只要：

   ```
   git add . && git commit -m "new post"
   git push
   quarto publish gh-pages
   ```

## 四、日常寫作流程

1. 複製 `posts/_template/` 資料夾，改名成 `posts/2026-09-your-slug/`（資料夾名建議用英文短名）。
2. 編輯裡面的 `index.qmd`：改標題、日期、分類，內文用 markdown 寫（Typora 寫好貼過來即可）。
3. 完成後刪掉 front matter 裡的 `draft: true` 那一行。
4. `quarto preview` 確認 → 依步驟三發佈。

## 五、待您修改的地方

- [ ] `_quarto.yml`：兩處 `USERNAME` 換成您的 GitHub 帳號
- [ ] `about.qmd`：`USERNAME`、Email、自我介紹
- [ ] 示範文章 `posts/2026-08-hello/` 確認功能正常後可整個資料夾刪除

## 六、日後擴充

- **教學講義**：可在同一 repo 加 `lectures/` 資料夾放 `.qmd`，或另建 Quarto `book` 專案。
- **研究論文**：`quarto use template quarto-journals/elsevier` 等期刊模板，同樣用 `.qmd` 寫。
- **圖檔說明**：見 `MANIFEST.md`。
