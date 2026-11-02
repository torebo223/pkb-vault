---
title: AntColony
type: project
created: 2026-11-02 10:46
updated: 2026-11-02 21:30
tags:
- project
- game
status: active
repos:
- AntColony
- AntColony-Unity
permalink: pkb/projects/ant-colony
---

# AntColony

## 概要
女王蟻1匹からコロニーを育てるリアルタイム MMO シミュレーション。春の結婚飛行で他プレイヤーの遺伝子と交配、PvP 襲撃で隣接コロニーと戦う。縦持ちスマホ、16×16px ピクセルアートの断面ビュー。

- `AntColony`: C# スクリプトと設計書（game_design.md）の置き場
- `AntColony-Unity`: 実際の Unity プロジェクト（スクリプトを取り込んで動かす）

> [!note] Claude: 2026-11-02 に torebo223/AntColony, torebo223/AntColony-Unity の README・CLAUDE.md・コミット履歴から下書き。違っていたら直してください。

## 現在の状況
- マージ済み: 成長バグ修正（#3）・食料庫建設（#4）・掘削の試作（#5）・URP の Pixel Perfect Camera（#6）・ドット絵（#8 → AntColony-Unity #2）
- **未マージ**: 創設パート（女王の着地から始まる）＝ AntColony #7 / AntColony-Unity #3（ブランチ claude/fix-growth-bugs-hlpp24）
- 2026-10-23: 六角形の森の世界マップと遠征（地図でマスをタップ→地形・距離・出る生き物、働き蟻を遠征に出して狩り・持ち帰り）を作成。PC の Unity でコンパイルは通った。riku が Unity で試すのを待っている（PR 化はまだ。PC 版とクラウド版の2つをまとめる必要あり）

## 次の一手
- [todo] 六角形マップと遠征を Unity で試す（右上「地図」→マスをタップ→「遠征隊を送る」）
- [todo] PC 側とクラウド側の2つの版を1つにまとめて PR にする
- [question] 降りる場所をマップで選ぶ形にするか（今はランダム）
- [question] アブラムシの扱い（Claude のおすすめ: 狩らずに、守ると甘露＝糖分をくれる仲間）
- [question] 六角形マップの作り込みはクラウドかPCか（カードで質問中。おすすめはクラウド）
- [todo] 創設パート #7 / Unity #3 をマージするか決める

## 決定事項
- [decision] 方向性: 「女王が指示して蟻が少しずつ掘り、穴が広がるのを眺める」のが好き（riku）
- [decision] ゲームは女王の「着地」から始める（2026-10-19 riku 選択）。最初の育児室・食料庫は廃止し、完成した女王室が食料100を持つ（初期食料100 = 57/29/14、容量100）。建設蟻0の間は女王は掘らない
- [decision] 女王は地表のすぐ下に女王室を1マスだけ掘る。深い部屋は働き蟻が掘り下げる。女王室は長押しで引っ越しできる。巣ビューは画面幅に合わせる（2026-10-23 riku 指定）
- [decision] 次の大きな要素は六角形の森の世界マップ＋地上・遠征。降りた場所で出る虫や動物が決まり、六角形マスを移動時間をかけて遠征する（2026-10-23）

## Observations
- [decision] 通信は Photon PUN 2。PUN2 が無くてもコンパイルが通るよう `#if PHOTON_UNITY_NETWORKING` でスタブに切り替え
- [fact] Photon AppId などの秘密情報はコードに書かない
- [fact] スクリプトは AntColony で書き、AntColony-Unity の Assets/Scripts/ に取り込む運用（2か所管理）。AntColony だけ直しても Unity には反映されない（2026-10-18 判明）。Scripts を変えたら AntColony-Unity にも同じ変更の PR を出す
- [fact] Unity プロジェクトはローカルの C:\Users\rikus\UnityProjects\AntColony（AntColony-Unity、Git LFS あり）。riku が別のローカルコピーを開いていたことがある
- [problem] PC の Remote Control とクラウドのスレッドで同じブランチを二重に直してしまった → [solution] コード修正はクラウド、PC は Unity 確認と Unity が生成した .meta・シーンのコミットだけ（2026-10-23）
- [problem] シーンの GameTimeManager.timeScale が 20（テスト用）のままだった（2026-10-23）
- [fact] ドット絵は Tools/pixelart/generate_sprites.py から PixelSprites.cs を自動生成。働き蟻3×3・兵隊6×5（ヨコヅナアリ風）・女王12×8、巣の中の卵・幼虫・食料は2〜5px

## Relations
- part_of [[index]]
- relates_to [[ゲーム]]

## 作業ログ
- 2026-09-27: 成長バグ修正（#3）、食料庫建設（#4）、掘削の試作（#5）
- 2026-09-28: Pixel Perfect Camera を URP 版に（#6）
- 2026-10-07〜08: ドット絵（#8、2026-10-19 マージ、Unity #2）
- 2026-10-19: 創設パート（#7 / Unity #3、未マージ）
- 2026-10-23: 女王室1マス・引っ越し、六角形の森マップと遠征（試作）
