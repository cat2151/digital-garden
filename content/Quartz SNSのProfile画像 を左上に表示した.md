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
    - 参考
        - 筆者の編集内容
            - [digital-garden/quartz/styles/custom.scss at v4 · cat2151/digital-garden · GitHub](https://github.com/cat2151/digital-garden/blob/v4/quartz/styles/custom.scss)
                - > // 左上に画像を表示
        - [[CSS調査のコツ]]
## プレビュー
- [[Quartz プレビュー手順]]
