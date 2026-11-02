---
title: quizjp
type: project
created: 2026-11-02 10:46
updated: 2026-11-02 10:46
tags: [project]
status: active
repos: [quizjp]
---
# quizjp

## 概要
「ご当地ピン（仮）」。日本のご当地もの（特産品・建造物・アニメ漫画のゆかりの地）の場所を地図にピンで当てるジオゲッサー風クイズ。PC ブラウザ向け、素の HTML/CSS/JS。距離スコア×市までの判定が差別化ポイント。

> [!note] Claude: 2026-11-02 に torebo223/quizjp の README・CLAUDE.md・コミット履歴から下書き。違っていたら直してください。

## 現在の状況
2026-10-24: モード（地方縛り・タイムアタック・デイリー）と図鑑・塗り地図を追加。ブラウザ版で完成させる方針。

## 次の一手
- [todo] 問題（data/questions.tsv）を増やす

## 決定事項

## Observations
- [decision] 当面はブラウザ版で完成させる（2026-10-24）
- [decision] 答えは「市」まで（町村は使わない、東京は特別区）（2026-10-23）
- [fact] index.html は生成物。src/ と data/ を直して `node tools/build.js`（座標が正解の市の外だとエラー）

## Relations
- part_of [[index]]

## 作業ログ

