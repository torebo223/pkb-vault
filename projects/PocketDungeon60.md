---
title: PocketDungeon60
type: project
created: 2026-11-02 10:46
updated: 2026-11-02 21:30
tags: [project, game]
status: active
repos: [PocketDungeon60]
---
# PocketDungeon60

## 概要
「60秒、1ダンジョン。通勤中に完結するローグライク。」iOS/Android、買い切り490円。Unity 6（6000.3.5f1）/ URP 2D / New Input System。

> [!note] Claude: 2026-11-02 に torebo223/PocketDungeon60 の README・CLAUDE.md・コミット履歴から下書き。違っていたら直してください。

## 現在の状況
リリース準備中。2026-10-05 に riku が「権限全部渡すから完成（ストア提出できる v1.0）まで全部やって」と Claude に任せた（実験）。
- マージ済み: リリース必須機能（#3）、Noto Sans JP への切り替えとリリース設定（#4）、リリース前バグ11件の修正（#5: 最終ボスのコイン、爆裂波の幽霊化、ボス二重強化、操作・表示まわり）、GitHub Actions の WebGL ビルド（#6）
- 2026-10-19: テスト用 APK（デバッグ署名）を PC でビルド済み（Builds\Android\PocketDungeon60.apk）
- 2026-10-23: GitHub Actions の初回ビルドが Unity へのログインで失敗（ライセンスは読めている、メール/パスワードが通らない）。**riku 待ち**
- ストア掲載文・プライバシーポリシーの下書きあり（Docs/ストア申請）

## 次の一手
- [todo] **riku**: GitHub のシークレット UNITY_EMAIL / UNITY_PASSWORD を直す。Google などでログインしているなら Unity ID でパスワードを作る、2段階認証はオフに。直したら「直した」と伝える
- [todo] Web 版をビルドして iPhone の Safari で開ける場所に置く（riku は iPhone しか持っていない）
- [todo] 実機テストと難易度調整
- [todo] Docs/バグ洗い出し_2026-10-19.md の未着手分（タイトル動画の mp4 化、セーフエリア対応 など）
- [todo] **riku**: ストア登録（Google Play $25 / App Store $99）、審査提出、プライバシーポリシー公開（文面は Claude が用意）

## 決定事項
- [decision] 「脱出」クリアは当面なし（ボス撃破のみ）。所持品は最大5個・ラン限定・使用で1ターン消費（2026-09-27）
- [decision] 確認なしで進めてよい。Claude が自分の PR を main にマージしてよい。ストア登録・課金・審査提出は riku 本人の操作（2026-10-08 riku「許可取りいらない」）
- [decision] フォントはメイリオ → Noto Sans JP（メイリオは同梱配布できずリリースの障害）（2026-10-08〜19）
- [decision] UnityConnectSettings の m_Enabled は 0 のまま（プライバシーポリシーの「解析なし」に合わせる。ビルドで1になるので注意）
- [decision] 進め方は A クラウドでコード → B riku の PC で Unity（フォント・Bundle ID・アイコン・実機テスト）→ C riku のみ（ストア・審査）

## Observations
- [fact] クラウドでは Unity エディタが使えない。変更後は PR に「Unityで確認すべきこと」を書く
- [fact] Asset Store 素材・フォント・動画はリポジトリに含まれない（ローカルのみ）。作業コピーは C:\dev\AIgame\PocketDungeon60（2026-10-19 に OneDrive 側から移動）
- [fact] クラウドでの C# 構文チェックは tree-sitter-c-sharp（pip）でやる。PR #5 はこの方法で確認してマージした
- [problem] Remote Control 側は、Claude 経由の指示だけだと git commit/push が自動許可で止まる → [solution] riku 本人がスレッドに一言（例「コミットプッシュ」）書けば通る（2026-10-19）

## Relations
- part_of [[index]]
- relates_to [[ゲーム]]

## 作業ログ
- 2026-10-05: 「完成まで全部」を任される。計画 A/B/C を提示
- 2026-10-08: #3 マージ。Noto Sans JP 切り替えの準備、Android ビルドのエディタスクリプト、アイコン
- 2026-10-19: #4 マージ、テスト APK ビルド、バグ洗い出し
- 2026-10-23: #5（バグ11件）・#6（WebGL ビルド）マージ。Actions の初回ビルドがログインで失敗

