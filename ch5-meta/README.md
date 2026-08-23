# ch5-meta｜Ch5 textkit-explain 的製作素材

> 這是 Ch5（特徵選擇）textkit-explain 版的「半透明後台」：
> 把 `ch5/` 互動講義背後的 **21 個原子知識點（KP）短稿** 與 **10 個示意圖 prompt** 整理公開，
> 讓讀者能看見「這份講義是怎麼寫出來的」。

---

## 📁 內容

```
ch5-meta/
├─ kp_drafts/             ← 21 個原子 KP 精簡短稿（11 站 × 2–4 KP）
│  ├─ S00/KP-S0-1.md … KP-S0-2.md    ← 站 0：為什麼選特徵
│  ├─ S01/KP-S1-1.md … KP-S1-2.md    ← 站 1：Peaking 現象
│  ├─ S02/… KP-S2-1 … KP-S2-2       ← 站 2：t-test
│  ├─ …
│  └─ S10/KP-S10-1.md … KP-S10-2.md  ← 站 10：BIC
│
└─ diagram_prompts/       ← 10 個示意圖 prompt（sketchnote 風格、16:9）
   ├─ KP-S0-1.md  ← 維度詛咒與 N/l 比
   ├─ KP-S1-1.md  ← Peaking 曲線
   ├─ KP-S2-2.md  ← t-test q 統計量
   ├─ KP-S3-1.md  ← ROC 曲線
   ├─ KP-S4-2.md  ← 散佈矩陣 J3
   ├─ KP-S5-1.md  ← SFS 子集選擇
   ├─ KP-S7-1.md  ← 離群值
   ├─ KP-S8-1.md  ← 隱藏層 = 非線性特徵生成器
   ├─ KP-S9-1.md  ← SRM 結構風險最小化
   └─ KP-S10-1.md ← BIC 損益兩平點
```

---

## 📐 排版規範（每個 KP 檔的固定骨架）

每個 `KP-S?-?.md` 都遵循這個結構（textkit-explain C2 規則）：

```markdown
# KP-S?-?｜<一句話標題>

| 項目 | 內容 |
|---|---|
| 一句話 | <一句話摘要> |
| 類比 | <類比名稱> |
| 公式 | <核心公式> |
| 口訣 | <口訣> |
| 誤解 | <最常見誤解> |

---

## 💡 一句話

（完整一句話，無符號）

---

## 🎭 類比（<類比名>）

（生活情境）

**對應理由**：<為什麼這個類比貼切>

---

## 📐 公式拆解

（每個符號白話化）

---

## 🔢 數值演算

（課本具體數字演算）

---

## 🤫 主動回想

（懸念鉤子或自問自答）

---

## 🎯 口訣

（一句話好記）

---

## ⚠️ 常見誤解

（學生最常踩的點）

---

## 圖

![圖 5.X：<caption>](assets/fig5.X_xxx.jpg)
```

> **關於摘要表**：5 行摘要表是給**純文字檔閱讀**用的（一眼能抓到 KP 在講什麼）。
> 但 `inject_kps.py` 注入到 HTML 互動講義時會**自動移除摘要表**（避免與下方 💡 一句話 H4 內容重複）。
> 所以 KP 短稿**必須保留摘要表**，但 HTML 部署後只會看到 7 個要素 + 課本附圖。

**規則速查**：

| 元素 | 規範 |
|---|---|
| H1 | 全檔只有 1 個：`# KP-S?-?｜<標題>` |
| 摘要表 | 緊接 H1、5 行：一句話／類比／公式／口訣／誤解（純文字檔閱讀用；HTML 注入時自動移除） |
| H2 | 7 個核心要素 + 可選 1 個「## 圖」段；核心要素 emoji 必須齊：`💡 🎭 📐 🔢 🤫 🎯 ⚠️` |
| 分隔 | 要素間用 `---` |
| 標頭 | 類比要素標題附帶類比名：`## 🎭 類比（老師帶學生）` |
| 對應理由 | 類比段落必含 `**對應理由**：` 標頭（AUDIT #57 強制） |
| 課本附圖 | `## 圖` 段放最後，內含 `![caption](assets/fig5.X_xxx.jpg)`；無對應圖放 placeholder 文字 |
| blockquote | 行數 ≤ 30%（禁止純 `>` 寫整段） |
| 每段長度 | 每個 H2 區塊 ≤ 800 字 |

**KP↔課本 fig 對映**（ch5）：

| KP | 對映 fig |
|---|---|
| KP-S1-1, S1-2 | fig5.1_peaking.jpg（Peaking 現象） |
| KP-S2-1, S2-2 | fig5.2_hypothesis.jpg（假設檢定接受/拒絕區間） |
| KP-S3-1 | fig5.3_roc.jpg（ROC 曲線） |
| KP-S4-1, S4-2 | fig5.5_scatter.jpg（$J_3$ 三種情況） |
| KP-S4-3 | fig5.6_fisher.jpg（Fisher 投影方向） |
| KP-S6-1 | fig5.7_projection.jpg（投影導致類別重疊） |
| KP-S9-1 | fig5.9_srm_tradeoff.jpg（SRM 權衡） |
| KP-S9-2 | fig5.8_srm.jpg（SRM 概念圖） |
| 其他 10 個 KP | 無對應課本 fig |

**稽核工具**：`textkit-explain/scripts/check_kp_format.py`

```bash
# 在 textkit-notes 公開版（ch5-meta/）跑：
python3 ~/.claude/skills/textkit-explain/scripts/check_kp_format.py ch5-meta/kp_drafts
# 預期輸出：✅ 通過：21 / ❌ 失敗：0
```

---

## 🎯 為什麼公開這兩個資料夾？

**textkit-explain** 與一般教學內容的差別在於「**寫作過程本身可被學習**」：

1. **KP 短稿的 6 要素結構**（一句話／類比＋對應理由／公式拆解／數值演算／主動回想／口訣＋常見誤解）是一種可遷移的寫作框架。
   - 想寫自己的技術筆記的讀者，可以拿這 21 個 KP 當**模板**。
2. **diagram_prompts/** 是 AI 生圖的「**文字稿**」。
   - 想用 gpt-image-2 / Agnes / Gemini 自己畫 sketchnote 風格示意圖的讀者，
     拿這 10 個 prompt 當**起點**，改寫成自己章節的版本。

---

## 📖 怎麼讀？

### A. 從成品出發（給一般讀者）

```
ch5-meta/kp_drafts/S00/KP-S0-1.md   ←  對應  ch5/index.html  站 0 的 KP 區塊
ch5-meta/diagram_prompts/KP-S0-1.md ←  對應  ch5/index.html  站 0 的示意圖佔位符
```

KP ID 的編號 `S0-1` = `站-該站第幾個`。例如 `KP-S7-3` = 站 7 的第 3 個 KP。

### B. 從方法論出發（給寫作者）

每個 KP 短稿的固定結構：

```markdown
# KP-S?-?｜<一句話標題>

> **一句話**：<一句話定義>
> **生活類比**：<具體情境>＋<為何對應>
> **公式拆解**：<每個符號的意義>
> **數值演算**：<兩個具體數字例子>
> **主動回想**：<1 題自我測試>
> **口訣**：<一句話記憶法>
> **常見誤解**：<初學者最常犯的錯>
```

### C. 從工具鏈出發（給工程師）

`diagram_prompts/*.md` 內的 `data-prompt` 區塊可直接餵給：

- `gpt-image-2`（ChatGPT 圖像模型）
- `Agnes 2.1 Flash`
- `Gemini 2.5 Flash Image`（Nano Banana）

產生後用 `base64 -w 0 < png` 編碼後替換 `ch5/index.html` 內的 `DIAGRAM_PLACEHOLDER`。

---

## ⚖️ 版權

- KP 短稿與 diagram prompt 皆為本作者原創（CC BY 4.0）
- 引用之課文／公式 / Example 數值版權屬 Theodoridis & Koutroumbas《Pattern Recognition》
- 公開目的是**教學方法論示範**，非取代課文

---

## 🔗 相關連結

- 成品（互動式網頁講義）：[`/ch5/`](../ch5/)
- 入口頁：[`/`](../)
- 課文原文：保留在本機 `ch5-textkit-explain/sources/`，**不公開**（版權考量）
