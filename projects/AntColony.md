---
title: AntColony
type: project
created: 2026-11-02 10:46
updated: 2026-11-02 10:46
tags: [project, game]
status: active
repos: [AntColony, AntColony-Unity]
---
# AntColony

## 概要
女王蟻1匹からコロニーを育てるリアルタイム MMO シミュレーション。春の結婚飛行で他プレイヤーの遺伝子と交配、PvP 襲撃で隣接コロニーと戦う。縦持ちスマホ、16×16px ピクセルアートの断面ビュー。

- `AntColony`: C# スクリプトと設計書（game_design.md）の置き場
- `AntColony-Unity`: 実際の Unity プロジェクト（スクリプトを取り込んで動かす）

> [!note] Claude: 2026-11-02 に torebo223/AntColony, torebo223/AntColony-Unity の README・CLAUDE.md・コミット履歴から下書き。違っていたら直してください。

## 現在の状況
2026-10-19〜23: 女王・働き蟻・兵隊・卵・幼虫・食料のドット絵を巣ビューに描画し、Unity 側に取り込み済み（AntColony PR #8 → AntColony-Unity PR #2）。

## 次の一手
- [todo] 次の実装範囲を決める（未記入）

## 決定事項

## Observations
- [decision] 通信は Photon PUN 2。PUN2 が無くてもコンパイルが通るよう `#if PHOTON_UNITY_NETWORKING` でスタブに切り替え
- [fact] Photon AppId などの秘密情報はコードに書かない
- [fact] スクリプトは AntColony で書き、AntColony-Unity の Assets/Scripts/ に取り込む運用

## Relations
- part_of [[index]]
- relates_to [[ゲーム]]

## 作業ログ

