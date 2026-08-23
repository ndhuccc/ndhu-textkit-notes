# DIAGRAM PROMPT for KP-S2-2｜t 分布接受區間，q=4.25 落在外

**Diagram ID**: diag-KP-S2-2
**Style**: schematic
**Aspect Ratio**: 16:9
**Used in**: ch5-textkit-explain interactive/index.html, part3 (站 2)

## data-prompt (English, for image generation models)

> A clean schematic on white background. Main element: a horizontal bell curve (t-distribution) drawn in light blue outline, centered at x=0, x-axis labeled "q statistic", range from -5 to +5. A central region between x=-2.10 and x=+2.10 is shaded light green and labeled "Acceptance region D=[-2.10, 2.10]". Two red dots are placed OUTSIDE the green region: one at x=+4.25 (labeled "q=4.25, Example 5.3, REJECT H0") and one at x=-4.25 (mirror, same label). Vertical dashed lines mark x=-2.10 and x=+2.10 with labels "t critical, df=18, alpha=0.05". Above the curve, an annotation reads "Beyond ±2.10 = significant difference". Below the curve, an annotation reads "Within ±2.10 = cannot reject H0". The bell curve is thin blue; the green region is light fill; the red dots are bold circles with thin black labels.

## 何時用
嵌入站 2「統計檢定選特徵（t-test）」的圖解區，緊接在 KP-S2-2 短稿之後。視覺化 Example 5.3 的 $q=4.25$ 與接受區間 $[-2.10, 2.10]$ 的相對位置——一眼看到「落在外頭->拒絕 $H_0$->特徵選中」。

## 後製產生
若環境有生圖工具，呼叫產生後用 `embed_assets.py` 替換為 base64。
若無，保留佔位符 + README 註明「示意圖待生成」。
