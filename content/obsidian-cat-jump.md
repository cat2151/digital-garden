- Bluesky
    - [@cat2151.bsky.social on Bluesky](https://bsky.app/profile/cat2151.bsky.social/post/3mcwqvxb7w22u)
## 用途
- page内を素早くjumpして遊ぶ用
    - 折りたたみ内にjumpしないとき用
    - headerのない巨大bullet listの途中にもjumpしたいとき用
    - 行頭にjumpしたいとき用
- jumpのプラグインを作って遊ぶ用
    - 楽しいよ！
## 状況
- まだlocalにのみ存在
- ドッグフーディング中
- 気が向いたら
    - GitHubリポジトリを作って、
        - そこに読みやすくリファクタリングした版を掲載する
            - という方向の想定
## 開発手順、備忘
- ※合計30分くらい
- 開発環境
    - 開く : プラグイン開発環境
        - ※過去に作ったもの。過去にプラグイン開発したことがあったので、そのときに作ったもの
    - backup : main.ts
        - ※今回ここに雑に上書きして作っていく
- 実装
    - Geminiにpromptを投げる。後述
    - 生成されたものを main.ts に貼り付ける
    - `num run build` する ※開発環境依存
- test
    - プラグインを有効化する
    - hotkeyにbindする
    - testする
    - バグってconsoleにerrorが出たので、それをGeminiに投げて修正させる
    - さらに2つバグが出たので、それをGeminiに投げて修正させる
    - 完成
- 本番環境
    - 開く : 自分のメインvaultのplugins
    - `cat-jump`という名前をつけてdirを作成
    - cp : main.js , manifest.json
    - edit : manifest.json
    - プラグインを有効化する
    - hotkeyにbindする
    - testし、installできたことを確認する
    - ドッグフーディングを開始する
## prompt
```
以下を参考に、obsidianのプラグインとなるmain.tsを生成してください。

機能：
    addCommand します。「jump」というcommandです。
    jump commandの機能：
        表示：
            ノートの行頭に、a-zA-Z をオーバーレイ表示します。
            見えている範囲の行のみを対象とします。
            折りたたまれている内部の行は対象外にします。
            つまり、見えている一番上がaとなり、折りたたまれている行はskipして、b,c,..となります。
        入力：
            1文字入力を待ちます。
        jump：
            入力された文字が a-zA-Z であれば、対応する行の行頭にjumpします。それ以外であればjumpしません。
            そしてオーバーレイ表示をやめて、もとの表示に戻ります。
            処理を終了します。
        debug：
            console.logに、要所を出力してデバッグ用とします。
    関数：
        単一責任の原則に従って関数分割します。
    以上です。


---------

※ここに自分の過去のプラグインのソースを貼り付けておく。
※例えば main.ts で完結する、シンプルで、addComand editorCallback タイプのものなど、
※今回生成させたいものと近いものがよい。
```
