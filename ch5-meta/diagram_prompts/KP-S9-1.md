# DIAGRAM PROMPT for KP-S9-1｜SRM 經驗誤差與複雜度權衡的 U 型曲線

**Diagram ID**: diag-KP-S9-1
**Style**: schematic
**Aspect Ratio**: 16:9
**Used in**: ch5-textkit-explain interactive/index.html, part10 (站 9)

## data-prompt (English, for image generation models)

> A clean schematic on white background showing a U-shaped curve. X-axis labeled "Model complexity (VC dimension, log scale)" from 0 to 10. Y-axis labeled "Generalization error" from 0 to 1.0. Three curves are drawn: (1) a thin gray dashed curve labeled "Empirical error (training)" that monotonically DECREASES from upper-left to lower-right, approaching 0 at high complexity; (2) a thin gray dashed curve labeled "Complexity penalty" that monotonically INCREASES from 0 at low complexity to about 0.8 at high complexity; (3) a BOLD red curve labeled "Generalization error (sum)" that forms a clear U-shape: starts high at low complexity (~0.7), drops to a minimum around complexity=3-4 (error ~0.15), then rises back to about 0.4 at high complexity. The minimum point of the red curve is marked with a red dot and labeled "SRM optimum". Vertical dashed lines connect the minimum to the x-axis. Top title: "Structural Risk Minimization (SRM)". Bottom annotation: "SRM picks the complexity that minimizes training + penalty, not just training error". Use thin lines, the red curve bold, the rest thin and gray.

## 何時用
嵌入站 9「泛化理論 SRM / SVM」的圖解區，緊接在 KP-S9-1 短稿之後。視覺化 SRM 的核心——泛化誤差是「經驗誤差（下降）+ 複雜度懲罰（上升）」的 U 型加總，最小值才是最佳複雜度。幫助讀者直觀理解「**不是訓練誤差越小越好**」這個反直覺的結論。

## 後製產生
若環境有生圖工具，呼叫產生後用 `embed_assets.py` 替換為 base64。
若無，保留佔位符 + README 註明「示意圖待生成」。
