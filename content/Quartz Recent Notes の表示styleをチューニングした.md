# 主観
- 1080pで7行程度しか表示できてない。20行はほしい
    - 全体にフォントがでかすぎ。小さく
    - 行間が広すぎ。狭く
    - スクロールバーがなくて混乱。つける
    - update日付は場所をとるだけで不要。先頭は全部昨日だし。外す
    - 長いノート名のせいで3行くらいが1ノートになってる。1行に収まるよう、10文字程度で切る
# 方法
- 前提知識
    - 公式
        - [Recent Notes](https://quartz.jzhao.xyz/features/recent-notes)
- 方法
    - `quartz\quartz\styles\custom.scss` を編集
        - デフォルトは空なので、LLMに上記を投げて生成させたものを貼り付ける
    - プレビュー： [[Quartz プレビュー手順]]
# 備忘
- 変更前の `quartz\quartz\styles\custom.scss`
```
@use "./base.scss";

// put your custom CSS here!
```
