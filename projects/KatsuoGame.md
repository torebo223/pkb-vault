---
title: KatsuoGame
type: project
created: 2026-11-02 10:46
updated: 2026-11-02 10:46
tags:
- project
- game
status: active
repos:
- KatsuoGame
permalink: pkb/projects/katsuo-game
---

# KatsuoGame

## 概要
高知・土佐沖でカツオ一本釣り漁船の船長として借金を返しながら漁業経営を立て直すシミュレーション。Unity 6 / URP 2D / TextMeshPro。

> [!note] Claude: 2026-11-02 に torebo223/KatsuoGame の README・CLAUDE.md・コミット履歴から下書き。違っていたら直してください。

## 現在の状況
2026-10-19: カツオの群れを探して追う仕組み、台風・大漁群・縄張り争いの選択、港の注文と銀行の返済期限を追加。釣りシーンの演出スクリプトも追加。2026-10-23 に重大バグ修正の PR をマージ。

## 次の一手
- [todo] 追加した仕組みを Unity で配線・確認（Docs/シーン配線手順.md）
- [todo] 経済バランスの調整（Docs/経済バランス検証.md）

## 決定事項

## Observations
- [fact] 商用フォント（モリサワ A-OTF ゴシックBBB）はリポジトリに含まれない
- [fact] 進行は GameManager の GamePhase: Port → Voyage → Fishing → ReturnAndSell → Management

## Relations
- part_of [[index]]
- relates_to [[ゲーム]]

## 作業ログ