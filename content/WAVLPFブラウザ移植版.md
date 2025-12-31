
# いろいろ
## whyを文書化しましょう
- 経緯
    - [@cat2151.bsky.social on Bluesky](https://bsky.app/profile/cat2151.bsky.social/post/3mbatmltwqk2b)

- why wavlpf？
　- 音色editうひょーというUXを提供するため
　- 過去に「このUXはうひょー」と実証済みであるため
　- 割り切ったコンパクトな仕様であり、実現可能性が高いため

- why wavlpf UX？
    - 別項を参照

## ADR
- [[ADR：WAVLPF：WAV生成において non-realtime render を採用する]]
- [[ADR：WAVLPF：曳光弾でなくプロトタイピングを採用する]]
- [[ADR：WAVLPF：ライブラリ作成を捨ててUX提供を目指す]]
- [[ADR：WAVLPF：高機能化・高性能化 を捨てて、Smile BASIC3版の仕様そのまま移植を目指す]]
## いろいろ
- 何かあれば

## why wavlpf UX？
- ※前提、今のモダンなedit UXとは大きく違う
- 実現可能性が高い
    - non-realtime に特化したUX

## wavlpfのUXの強みとは？
- decay edit
    - LPFのcutoff decay
    - 最低限これがマスト
    - wavlpfのenvelopeはdecayのみに割り切って絞った設計
- タッチペンデバイス
    - ※アレンジは必要そう、タッチ場所を大きくする等
    - ブラウザでマウス、スマホでタッチ、でいける想定

## 済 agentに投げた初手の500文字
```prompt
- 私が過去に作ったソフトシンセ WAVLPF をTypeScriptで実装していく準備をします
- 小さく始めるため、音の出る簡易ソフトシンセを実装してください
- 500msecごとにwavを生成し、Tone.jsで演奏する
- 生成方式
    - WebAudio非依存の信号処理関数を実装しnon-realtime renderする
- wav内容
    - 500ms、220HzのSawtooth生成関数を実装しrender
    - それにBiquad FilterのLPF関数を実装し適用
        - LPF処理
            - 初期値
                - mouse x,yを利用
                    - xはCutoff freq.で20Hz～1000Hz、yはResonanceで、LPFのQ値 0.5～2
            - Cutoff freq. Decay
                - 初期値から、1msごとに1Hz減衰し、1Hzがmin
```
