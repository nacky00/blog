---
title: "【Googleスプレッドシート】数字の値に応じた文字列を設定する"
date: 2021-12-26T13:45:00+09:00
draft: false
---

## 完成イメージ

![完成イメージ](/posts/img/2021-12-26-spreadsheet-01.png)

## 使用する関数
- [ARRAYFORMULA関数](https://support.google.com/docs/answer/3093275?hl=ja)
- [IF関数](https://support.google.com/docs/answer/3093364?hl=ja)
- [IFS関数](https://support.google.com/docs/answer/7014145?hl=ja)

## 入力例

```
=ARRAYFORMULA(IF(A2:A<>"", IFS(B2:B>=500,"500以上",B2:B>=100,"100以上500未満",B2:B>=50,"50以上100未満",B2:B>=20,"20以上50未満",TRUE,"20未満"), ""))
```