# DIAGRAM PROMPT for KP-S5-1｜SFS 流程：每次選增益最大的特徵

**Diagram ID**: diag-KP-S5-1
**Style**: schematic (flow diagram)
**Aspect Ratio**: 16:9
**Used in**: ch5-textkit-explain interactive/index.html, part6 (站 5)

## data-prompt (English, for image generation models)

> A clean horizontal flow diagram on white background showing 4 sequential steps of the Sequential Forward Selection (SFS) algorithm. From left to right, four large rounded rectangles labeled "Step 1", "Step 2", "Step 3", "Step 4". Each rectangle contains: the selected feature number, the cumulative criterion value, and a small bar chart of the 8 candidate features with the selected one highlighted in red. Step 1: "Select f1 (FDR=0.71), J=0.71". Step 2: "Select f0 (FDR=0.54), J=1.25". Step 3: "Select f2 (FDR=0.37), J=1.62". Step 4: "Select f6 (FDR=0.01, noise!), J=1.63" — this last step has a small warning icon (⚠) next to the rectangle. Arrows connect the steps left to right. Above the flow, a title: "SFS: greedy, never backtracks". Below the flow, a note: "After 3 useful features, SFS may pick a noise feature as the 4th — floating search fixes this". The schematic should use thin black lines with red highlight for selected features. No 3D, flat design.

## 何時用
嵌入站 5「特徵子集選擇 SFS」的圖解區，緊接在 KP-S5-1 短稿之後。視覺化 SFS 4 步貪婪過程——特別是「選到雜訊」這個失敗案例，預示浮動搜索要解決的問題。

## 後製產生
若環境有生圖工具，呼叫產生後用 `embed_assets.py` 替換為 base64。
若無，保留佔位符 + README 註明「示意圖待生成」。
