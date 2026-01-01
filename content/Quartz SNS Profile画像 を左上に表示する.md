- やりたいこと
    - Quartz左上にSNS Profile画像 を表示したい
- 調査
    - LLMにきいた
- 検証
    - ハルシネーション多発
    - 対策
        - chrome dev toolsで
            - 当該部分の要素のstylesのスクショをとり
                - LLMに投げた
    - 解決した
# 手順
## 配置
- 画像
    - `quartz\public\static\cat.jpg`
        - 256x256
## 編集
- `quartz\quartz\styles\custom.scss`
## プレビュー
- [[Quartz プレビュー手順]]

# TODO 編集内容はあとでgithubのlink、上記のscssをlinkに貼る
