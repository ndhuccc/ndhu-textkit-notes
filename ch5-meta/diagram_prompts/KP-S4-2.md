# DIAGRAM PROMPT for KP-S4-2｜三種散分布 a/b/c 對照圖

**Diagram ID**: diag-KP-S4-2
**Style**: sketchnote
**Aspect Ratio**: 16:9
**Used in**: ch5-textkit-explain interactive/index.html, part5 (站 4)

## data-prompt (English, for image generation models)

> A sketchnote-style illustration on white background with black ink lines and light red accent color, organized in three side-by-side panels labeled (a), (b), (c), each showing two class clusters in 2D space. Panel (a): two small tight circles (sigma=0.3) labeled "omega1" (red) and "omega2" (blue) very close together (centers 0.5 apart). Above panel (a): hand-written label "Class-in tight, class-between near" and value "J3 = 164.7". Panel (b): two large loose circles (sigma=2.0) labeled "omega1" (red) and "omega2" (blue), still close together (centers 0.5 apart), but each cluster spread out. Above panel (b): label "Class-in loose, class-between near" and "J3 = 12.5" (marked with a frown). Panel (c): two small tight circles (sigma=0.3) labeled "omega1" (red) and "omega2" (blue), far apart (centers 3.0 apart). Above panel (c): label "Class-in tight, class-between far" and "J3 = 620.9" (marked with a star). Bottom of figure: hand-written equation "J3 = trace(Sw$^{-1}$ Sm) — bigger = better separated". Use simple geometric shapes, hand-drawn style, no fancy 3D shading.

## 何時用
嵌入站 4「類別可分離度量」的圖解區，緊接在 KP-S4-2 短稿之後。視覺化 Example 5.5 的三種 2D 分布對照——一眼看出 $J_3$ 大小與「類間遠近 x 類內鬆緊」的對應關係。

## 後製產生
若環境有生圖工具，呼叫產生後用 `embed_assets.py` 替換為 base64。
若無，保留佔位符 + README 註明「示意圖待生成」。
