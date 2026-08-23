# DIAGRAM PROMPT for KP-S0-1｜維度詛咒與 N/l 比

**Diagram ID**: diag-KP-S0-1
**Style**: sketchnote
**Aspect Ratio**: 16:9
**Used in**: ch5-textkit-explain interactive/index.html, part1 (站 0)

## data-prompt (English, for image generation models)

> A sketchnote-style flat illustration on white background with black ink lines and one accent red color. The scene shows ONE university professor at a desk distributing experiments to students. Left half: professor happily distributing 5 experiments to each of 9 students (small group), each student doing well, students raising hands confidently — labeled "N=100, l=9, N/l=11, OK". Right half: the SAME professor forced to distribute only 2 experiments to each of 50 students (large group), students looking confused and bored, professor sweating — labeled "N=100, l=50, N/l=2, students only memorize but don't understand". Between the two halves, a large red label reads "N/l is samples per parameter". Below the scene, a hand-drawn line chart showing test error vs number of features (l): y-axis "Test Error", x-axis "l", curve goes DOWN then UP forming a hill/mountain shape, minimum point marked with a red star and labeled "optimal l ~= N/alpha". Bottom caption: "Curse of Dimensionality — too many features for too few samples".

## 何時用
嵌入站 0「為什麼要選特徵」的圖解區，緊接在 KP-S0-1 短稿之後，幫助讀者把抽象的 $N/l$ 比變成「每位學生分到幾個實驗」的可見類比。**短稿用「老師帶學生做實驗」類比，圖解必須用同一類比**——不能混搭舊版「貨車載箱子」。

## 後製產生（用 gpt-image-2 / Agnes 2.1 / Gemini）
若環境有生圖工具，呼叫產生後用 `embed_assets.py` 替換為 base64。
若無，保留佔位符 + README 註明「示意圖待生成」。
