---
title: CofeGame
type: project
created: 2026-11-02 10:46
updated: 2026-11-02 21:30
tags:
- project
- game
status: active
repos:
- CofeGame
permalink: pkb/projects/cofe-game
---

# CofeGame

## 概要
スマホ（縦持ち）向けの放置寄りカフェ経営シミュレーション。仮タイトル「借金からはじめるカフェ」。
「借金500万円、空き店舗ひとつ。自分だけのカフェで返済を目指す。」プレイヤーは社長で、店に立つのは社員。1週間が1サイクルで、週末に社員ミーティング（売上・要望・トラブル報告）。ドット絵の見下ろし店内、店内レイアウトはプレイヤーが配置する。Unity 6 / URP 2D。

- 企画書 v0.5（2026-09-28）: 共有フォルダ cafe/企画書.md（まだリポジトリには入れていない）
- ブラウザのお試し版（HTML）: https://claude.ai/artifact/3GwBuWLBVVbEoP7VGd5h8o
- リポジトリ CofeGame は Unity の初期状態（サンプルシーン）のみ。企画時は名前を「CafeGame」と決めていたが、実際は CofeGame で作られた

> [!note] Claude: 2026-11-02 に torebo223/CofeGame の README・CLAUDE.md・コミット履歴から下書き。違っていたら直してください。

## 現在の状況
企画書たたき台とブラウザお試し版まで。Unity 版は未着手（2026-09-28 以降止まっている）。

## 次の一手
- [todo] 企画書の「作る順番」1: 絵なしの試作（四角の客が来て、座って、払って帰る。7日営業で週末ミーティング）→「眺めていて楽しいか」を確かめる
- [question] タイトル（仮「借金からはじめるカフェ」）
- [question] 売り方: 買い切り／無料＋広告／まだ決めない
- [question] 営業中の1日の長さ（仮: 現実で約1分）
- [question] 社長も店に立てるか（仮: タップで手伝えるだけ）

## 決定事項
- [decision] 舞台は架空の街。アプリを閉じている間は営業が進まない（2026-09-28）
- [decision] 店内レイアウト（テーブル・カウンター・レジ・植物）はプレイヤーが1マス単位で配置。歩く距離が待ち時間になる（2026-09-28）
- [decision] スタッフはレア度 N/R/SR/SSR・レベル・経験値・能力値（接客/バリスタ/調理）・資格を持ち、求人で雇う。5人まで（2026-09-28）
- [decision] 月末に払えないときは「追加融資／閉店」（KatsuoGame と同じ考え方）。返済期限3年＝ゲーム内36か月

## Observations
- [fact] 流用元: KatsuoGame の FinanceManager（資金・借金・固定費）・GameManager（日付）・SaveManager（オートセーブ）、AntColony のドット絵規格（16×16px）と MobileUILayout（セーフエリア）、PocketDungeon60 のスマホ入力
- [fact] 数値はすべて仮。「要確認」は riku が決めるまで実装しない

## Relations
- part_of [[index]]
- relates_to [[ゲーム]]

## 作業ログ
- 2026-09-28: 企画開始（スレッド「新しいゲームの企画」）。企画書 v0.5 とブラウザお試し版。リポジトリ CofeGame を初回チェックイン
