# 國中升學決策表

一頁式的靜態網站：協助家長在**公立國中、私立中學、國際學校、實驗教育學校、自學**之間做選擇。

不提供排名，也不比較哪一所學校比較好。它做兩件事：

1. 把「聽說某某比較好」拆成可以查證的成分（篩選效應 vs 時間堆疊 vs 進度密度 vs 師資一致性）。
2. 用**退出成本**排序各條路徑，讓不可逆的決定盡量往後推。

## 功能

- 五題孩子特質觀察，每題附判讀說明
- 五條路徑卡，含費用、時程、退出成本（1–5 級）、適合／不適合、該去問什麼
- 退出成本階梯
- 常被忽略的升學管道（資優班、科學班、直升、五專、技職、海外、同等學力）
- 父母對齊欄位，含「退場條件」
- 時程檢核清單

勾選與筆記存在瀏覽器的 `localStorage`，**不會上傳到任何伺服器**。
「複製分享連結」會把整份進度編碼進網址 hash，可以直接傳給另一半。

## 內容與資料來源

本站整理自公開的升學制度資訊。招生方式、費用與申請時程各縣市與各校差異大且逐年調整，
**決策前請以當年度官方簡章與學校說明為準**。

## 開發

純靜態，無建置步驟。網站根目錄是 `docs/`。

```bash
npx serve docs
```

## 部署

程式碼在 GitHub，由 **Cloudflare Pages 的 Git 連結**自動部署。push 到 `main`，
Cloudflare 會自己拉取並發布——不需要 API token，也不需要 GitHub Actions。

| 設定項 | 值 |
| --- | --- |
| Production branch | `main` |
| Framework preset | None |
| Build command | （留空） |
| Build output directory | `docs` |

GitHub Pages 亦由 `main` 分支的 `/docs` 提供，作為備援。
不需要的話可到 repo 的 Settings → Pages 關閉。

## 授權

內容採 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh-hant)，程式碼採 MIT。
