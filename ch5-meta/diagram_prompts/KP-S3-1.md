# DIAGRAM PROMPT for KP-S3-1｜ROC 完美分類：曲線貼左上角

**Diagram ID**: diag-KP-S3-1
**Style**: schematic
**Aspect Ratio**: 1:1
**Used in**: ch5-textkit-explain interactive/index.html, part4 (站 3)

## data-prompt (English, for image generation models)

> A clean schematic on white background. A square plot area 400x400 pixels, x-axis labeled "False alarm rate (a)" 0 to 1, y-axis labeled "Hit rate (1-beta)" 0 to 1. Three ROC curves are drawn in the same axes: (1) a thin gray dashed diagonal line from (0,0) to (1,1) labeled "Random guess, AUC=0.5"; (2) a medium blue smooth convex curve from (0,0) curving up through (0.1, 0.7), (0.3, 0.9), (0.6, 0.95), to (1,1) labeled "Moderate, AUC=0.85"; (3) a bold red curve hugging the top-left corner from (0,0) sharply up to (0,1) then right to (1,1) labeled "Perfect, AUC=1.0". The area under the perfect curve is lightly shaded red. Small arrows point to each curve with their labels. The plot title: "ROC Curves: Better classifier = more bowed toward top-left". No grid lines except faint ones at 0, 0.5, 1.0.

## 何時用
嵌入站 3「ROC 曲線」的圖解區，緊接在 KP-S3-1 短稿之後。視覺化三條 ROC 曲線（亂猜、中等、完美）對應不同 AUC 值的差異——一眼看到「曲線越拱、特徵越能分」。

## 後製產生
若環境有生圖工具，呼叫產生後用 `embed_assets.py` 替換為 base64。
若無，保留佔位符 + README 註明「示意圖待生成」。
