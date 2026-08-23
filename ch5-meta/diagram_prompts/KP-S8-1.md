# DIAGRAM PROMPT for KP-S8-1｜神經網路自動把特徵工程與分類合在一起

**Diagram ID**: diag-KP-S8-1
**Style**: sketchnote
**Aspect Ratio**: 16:9
**Used in**: ch5-textkit-explain interactive/index.html, part9 (站 8)

## data-prompt (English, for image generation models)

> A sketchnote-style flow diagram on white background with black ink lines and one accent red color. Compare two parallel flows stacked vertically. Top flow labeled "Traditional ML (manual features)": boxes connected by arrows: [Raw data] -> [Hand-crafted features (HOG, SIFT)] -> [Classifier]. Each box has a small hand icon on it, indicating "human picks the features". Bottom flow labeled "Deep Learning (automatic features)": [Raw data] -> [Hidden layers (neural network)] -> [Output prediction]. The hidden layers box is shaded red and labeled "auto-learned features", with a small robot/gear icon. Between the two flows, a large hand-drawn arrow with label "Hidden layers = automatic feature engineering". At the bottom, a single-line summary: "Traditional: human designs features -> DL: network learns them". Use simple geometric shapes, hand-drawn style with slight imperfections, no 3D shading.

## 何時用
嵌入站 8「神經網路與特徵生成」的圖解區，緊接在 KP-S8-1 短稿之後。視覺化對比「傳統 ML 手工選特徵」vs「深度學習自動學特徵」——一眼看出隱藏層的角色。

## 後製產生
若環境有生圖工具，呼叫產生後用 `embed_assets.py` 替換為 base64。
若無，保留佔位符 + README 註明「示意圖待生成」。
