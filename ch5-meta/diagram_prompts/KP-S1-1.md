# DIAGRAM PROMPT for KP-S1-1｜錯誤率隨特徵數先降後升

**Diagram ID**: diag-KP-S1-1
**Style**: schematic (line plot with annotations)
**Aspect Ratio**: 16:9
**Used in**: ch5-textkit-explain interactive/index.html, part2 (站 1)

## data-prompt (English, for image generation models)

> A clean schematic line plot on white background with black axes. X-axis labeled "Number of features (l)" ranges from 0 to 30. Y-axis labeled "Test error rate" ranges from 0 to 1.0. A single smooth blue curve forms a clear U-shape (valley): starts high at l=1 (around 0.35), decreases steadily to a minimum at around l=8-10 (error ~0.08), then rises back up to about 0.30 at l=30. The minimum point is marked with a red dot and a label "OPTIMAL POINT". Three colored dots are placed at l=1, l=optimal, l=30, labeled with their error values. In the upper-right corner, a small equation box shows "l* ~= N/alpha, alpha in [2, 10]". Top title: "Peaking Phenomenon". The blue curve is bold; the rest is thin black lines.

## 何時用
嵌入站 1「Peaking 現象」的圖解區，緊接在 KP-S1-1 短稿之後。作為 Figure 5.1 的視覺化補充（Figure 5.1 是課本原圖，這張是「理想化曲線」幫助讀者一眼看到關鍵形狀：先降後升 + 最低點）。

## 後製產生
若環境有生圖工具，呼叫產生後用 `embed_assets.py` 替換為 base64。
若無，保留佔位符 + README 註明「示意圖待生成」。
