# 方法
- ※LLMに調査させたのち、情報不足だったので人力調査した結果
- `quartz.layout.ts`
    - Explorerを外し、
    - RecentNotesを追加する
```
// Component.Explorer(),
Component.RecentNotes({ limit: 20 }),
```
# [[ADR]]
- 経緯
    - Quartz 左のExplorerがアルファベット順なのが邪魔、自分の用途にマッチしないと感じる
- 背景
    - timestamp降順にする方法として、RecentNotesがある
    - ExplorerとRecentNotesを両方表示するか、RecentNotesだけ表示するか、を選べる
    - Searchはそのまま維持するので、全noteの検索はこれまでどおり可能である
- 決定
    - Explorerを削除し、かわりにRecentNotesを追加する
- 却下した選択肢
    - ExplorerとRecentNotesを両方表示する
        - デメリット
            - 自分の用途にマッチしない
                - 自分の用途
                    - フラットなノート配置
                    - ファイル名ソートを意識しないノート名
                    - 最近編集したノートに素早くアクセス、という体験を閲覧者に提供したい
            - Explorerはあるだけ邪魔（自分の用途に限っては、の話）
- 影響
    - メリット
        - 最近の20件のノートを表示できる
            - 前述の自分の用途にマッチした使い方ができる
    - デメリット
        - Explorerによる全ノートの一覧表示の恩恵がなくなる
