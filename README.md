# 模式辨認自學講義（公開版）

> 開放性教材：**互動式講義（HTML）＋ 手把手 Python 筆記本**。
> 原始教材（教科書全文）不在此公開；本倉庫僅含自行整理之教學素材。

## 📖 單元

| 單元 | 講義 | 筆記本 |
|---|---|---|
| 第一章 導論 | [ch1/index.html](ch1/index.html) | `ch1/nb0_熱身` ～ `ch1/nb3_迷你專案` |
| 第七章 特徵產生 II | [ch7/index.html](ch7/index.html) | `ch7/nb0_熱身` ～ `ch7/nb4_迷你專案` |

線上瀏覽講義：
- https://mitlab323.github.io/textkit-notes/ch1/
- https://mitlab323.github.io/textkit-notes/ch7/

## 🧪 執行筆記本

```bash
pip install -r ch1/requirements.txt   # 或 ch7/requirements.txt
jupyter notebook ch1/                 # 或 ch7/
```

> 筆記本全部使用合成資料，不需下載外部檔案。

## 🚀 自動部署

本倉庫啟用 GitHub Actions 自動部署 GitHub Pages（`.github/workflows/pages.yml`）：

- 觸發：`push` 到 `main`（僅當 `index.html`、`ch*/index.html`、`ch*/katex/**`、`ch*/assets/**`、`ch*/requirements.txt`、`README.md`、workflow 本身變更時才會跑）
- 也可手動觸發：Actions → Deploy GitHub Pages → Run workflow
- 首次啟用：到 GitHub repo 的 **Settings → Pages → Source** 切換為 **GitHub Actions**

部署完成後的網址：

- 入口：https://mitlab323.github.io/textkit-notes/
- 各章節：`/ch1/`、`/ch2/`、`/ch3/`、`/ch4/`、`/ch7/`

## ⚖️ 聲明
- 講義與筆記本為作者依 Theodoridis & Koutroumbas《Pattern Recognition》自行整理之學習教材；課文全文（sources）不在此公開，講義內僅含以教學目的引用之必要圖例與自行撰寫的解說。
- 公式由本機 KaTeX 渲染（`ch*/katex/`），不需 CDN，離線可看。
