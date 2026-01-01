# 実施のモチベ
- [[ADR：Quratz：Recent Notesを追加する]]

# 方法
- ※LLMに調査させたのち、情報不足だったので人力調査した結果
- `quartz.layout.ts`
    - Explorerを外し、
    - Recent Notesを追加する
```
// Component.Explorer(),
Component.RecentNotes({ limit: 50 }),
```
- limit
    - 当初20行にしていた
        - 少ないと感じて50行にした
            - きっかけ : [[Quartz Recent Notes の表示styleをチューニングした]]
- 表示styleのチューニング
    - [[Quartz Recent Notes の表示styleをチューニングした]]

