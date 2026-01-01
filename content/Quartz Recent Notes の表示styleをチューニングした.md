# チューニングのモチベ
- ※主観
    - これまでの課題と、ほしいもの
        - 1080pで7行程度しか表示できてない。20行はほしい
            - 全体にフォントがでかすぎ。小さく
            - 行間が広すぎ。狭く
            - スクロールバーがなくて混乱。つける
            - update日付は場所をとるだけで不要。先頭は全部昨日だし。外す
            - 長いノート名のせいで3行くらいが1ノートになってる。1行に収まるよう、10文字程度で切る
    - チューニングが解決すること
        - 上記の「ほしいもの」を獲得できる
# 方法
- 前提知識
    - 公式
        - [Recent Notes](https://quartz.jzhao.xyz/features/recent-notes)
- 方法
    - 編集
        - `quartz\quartz\styles\custom.scss` を編集
            - デフォルトは空なので、LLMに上記を投げて生成させたものを貼り付ける
    - プレビュー： [[Quartz プレビュー手順]]
## 表示styleチューニングのコツ
- もしわからないことがあれば、
    - ブラウザの開発モードでli要素などのstylesのスクショをとり、
        - それをLLMに投げつけて調査させる
            - ※今回筆者はClaudeを使ったが、ほかのLLMでもよいだろう
## [[Quartz Recent Notes 横スクロールバー]]
# 関連
- [[Quartz 左のExplorerをアルファベット順でなく、timestamp降順にした（Recent Notesを利用）]]
    - スクロールバーをつけた結果、20行でなく50行ほしいと感じたので、
        - 上記で50行に設定した
# 参考
- 筆者の設定
    - [digital-garden/quartz/styles/custom.scss at v4 · cat2151/digital-garden · GitHub](https://github.com/cat2151/digital-garden/blob/v4/quartz/styles/custom.scss)
