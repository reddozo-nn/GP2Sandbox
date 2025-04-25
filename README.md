# GP2Sandbox

Unityでのチーム開発やオブジェクト指向、SOLID原則を学ぶためのサンプルプロジェクトです。

## 前提条件
- GitHubのアカウントを持ち、基本的な操作ができること
- Unity6以降の基本操作ができること
- [WinMerge](https://winmergejp.bitbucket.io/)がインストールされていること

## 作業準備
チュートリアルをはじめる前にやっておく準備手順です。

1. GitHubにサインインして、このリポジトリーをForkします
1. GitHub Desktopなどでクローンします
1. 今回は自分達の学習に利用するので、下の **For my own purposes** を選択して Continue します

![プルリクエスト先を自分のリポジトリーへ](Documents/images/img00.png)

4. Unity Hubを起動して、追加 > ディスクから加える をクリックして、クローンしたフォルダーを開く
5. プロジェクトに、GP2Sandboxが追加されるので、それをクリックして、プロジェクトを開く
7. エディターバージョンを変更しますか？　が表示されたら、バージョンを変更をクリック
1. Unityが開いたら、Windowメニューから TextMeshPro > Import TMP Essential Resources を選択して Import します
1. Projectウィンドウから GP2Sandbox > Scenes フォルダーを開いて、 System シーンをダブルクリックして開きます

以上で準備完了です。Playすればプロジェクトが起動します。


## 操作方法
- 画面クリックでゲーム開始
- プレイヤーはマウスカーソルの方向に向きます
- クリックで弾を撃ちます
- 弾を撃つと反動で逆方向に加速します
- デバッグキーとして、O(オー)キーでゲームオーバー、Cキーでクリアします

以上です。キャラクターの破壊処理はまだ入っておらず、ゲームとしては未完成です。


## このプロジェクトでやりたいこと
- [GitHub練習](./Documents/github_practice.md)
  - ブランチ操作
  - コンフリクトの発生と解決方法、対策
- unitypackageへのエクスポートによる共同開発
- オブジェクト指向の機能確認
  - カプセル化、継承、ポリモーフィズム
  - インターフェースによる処理の実装の分離
- ジェネリック
  - GetComponentで利用済み
  - IShooter, NormalShooterとNormalShotAssetで実装を確認
- SOLID原則
  - 単一責任
    - プレイヤーとショット
  - オープン・クローズドの原則
    - MonoBehaviour
  - リスコフの置換原則
    - 様々なオブジェクトを管理できるAM1ObjectPool
  - インターフェース分離の原則
    - プレイヤーや敵の行動の分離
  - 依存関係逆転の原則
    - 上位のGameParamsからScoreTextを参照するのではなく、ScoreTextからGameParamsへ依存する

## サンプルアプリ
### 操作方法
- マウスで操作
- プレイヤーはマウスの方向を向く
- クリックでショット
- 敵や敵の弾に当たったらゲームオーバー
- 敵を全て倒したらクリア
- スコアを競う

## LICENSE
[MIT License](./LICENSE)

Copyright (c) 2021 Yu Tanaka
