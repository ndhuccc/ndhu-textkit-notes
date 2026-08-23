# DIAGRAM PROMPT for KP-S7-1｜前處理三步驟流程

**Diagram ID**: diag-KP-S7-1
**Style**: schematic (flow diagram)
**Aspect Ratio**: 16:9
**Used in**: ch5-textkit-explain interactive/index.html, part8 (站 7)

## data-prompt (English, for image generation models)

> A clean horizontal flow diagram on white background showing 3 sequential preprocessing steps connected by arrows. Step 1 (left, labeled "1. Outlier Removal"): a scatter plot with most points clustered normally plus 3 red dots far from the cluster (representing outliers at z-score > 3), with a red "X" over the outliers and an arrow leading to Step 2. Step 2 (middle, labeled "2. Normalization"): two mini histograms side by side: left shows raw data with different scales (e.g., one tall thin bar at 100, another short wide bar at 0.5), right shows normalized data with both bars at similar height (z-score or min-max). Arrow to Step 3. Step 3 (right, labeled "3. Missing Value Imputation"): a data table with 3 cells marked "NaN" in red, and a green arrow showing those cells filled with median values. Below the whole flow, a single-line caption: "Clean -> Normalize -> Impute -> Train". Use thin black lines with red for "before" states, green for "after" states. Flat 2D design, no 3D.

## 何時用
嵌入站 7「前處理」的圖解區，緊接在 KP-S7-1 短稿之後。視覺化前處理三步驟（離群值移除 -> 正規化 -> 缺值填補）的順序——幫助讀者建立「先清菜、再下鍋」的心智模型。

## 後製產生
若環境有生圖工具，呼叫產生後用 `embed_assets.py` 替換為 base64。
若無，保留佔位符 + README 註明「示意圖待生成」。
