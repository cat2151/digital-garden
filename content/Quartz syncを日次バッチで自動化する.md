
# モチベ
- これまでの課題
    - syncを手で入力していた
        - メリット
            - 自分で公開タイミングを選べる
        - デメリット
            - 選択疲労が発生する
- 自動化のメリット
    - 疲労防止
        - [[決断疲労]] を防止できる
    - ユーストレス
        - 「常に公開状態の記事を書く」という [[ユーストレス]] を得られる
    - ラバーダッキング
        - 常に公開状態であることは、 [[Bluesky]] 同様に、[[ラバーダッキング]] の恩恵が得られるということ
            - つまり、よりよい文章を書きやすくなることが期待できる
# 例
- [[cat-file-watcher]] を利用する
- 設定ファイル例
    - 夜中に1回～2回自動でsyncする
        - ※これからtestする
```toml
[[commands]]
    # 実行 : digital-garden sync（Obsidian Quartz）
    command             = 'start "" cmd /c npx quartz sync'
    cwd                 = "C:/projects/quartz/"
    time_period         = "night_shift"
    interval            = "3h"
    no_focus    = true
```
