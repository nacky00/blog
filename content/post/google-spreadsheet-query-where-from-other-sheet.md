---
title: "Google Spreadsheet Query Where From Other Sheet"
date: 2021-05-24T11:03:20+09:00
draft: true
---

```
=QUERY('②【P,R,Q,T,U記入】PlaceIDと座標確認'!1:1000,"select A, B, D, E, F, L, S, V, W where S <>'' and ( F = '" & JOIN("' or F = '", QUERY('【参照】食べログ取得除くジャンルの指定'!A2:B,"select A where B = true")) & "')")
```