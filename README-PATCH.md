# 本次更新內容與安裝步驟

## 包含檔案

| 檔案 | 放到專案的位置 | 作用 |
|---|---|---|
| posts/2026-08-answers-cheap/index.qmd | 同路徑（新增資料夾） | 第一篇正式文章〈答案變便宜之後〉 |
| posts/_metadata.yml | 同路徑（新增檔案） | 所有文章自動加上 giscus 留言區 |

把 `posts` 資料夾整個複製到您的 `ai-blog` 專案裡合併即可。

## giscus 留言功能：需先在 GitHub 做兩個開關（各約 30 秒）

1. **開啟 Discussions**：
   repo 頁面 → Settings → General → 往下捲到 Features → 勾選 **Discussions**

2. **安裝 giscus App**：
   打開 <https://github.com/apps/giscus> → Install →
   選「Only select repositories」→ 選 **ai-blog** → Install

## 發佈

在專案資料夾執行：

```
quarto render
git add .
git commit -m "post 1 + giscus comments"
git push
```

等 1-2 分鐘後重新整理網站。打開文章捲到最底，應可看到留言區
（需用 GitHub 帳號登入才能留言——學生多半都有）。

## 順手清理（可選）

示範文章功能已驗證完畢的話，可刪除 `posts/2026-08-hello/` 整個資料夾。
