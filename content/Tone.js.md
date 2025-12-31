- GitHubリポジトリ
    - [GitHub - Tonejs/Tone.js: A Web Audio framework for making interactive music in the browser.](https://github.com/Tonejs/Tone.js/)
# 持論
## [[DSP]]書けない
- 実際は書いて連携は、ある程度はできるらしい
- 基本的に「できない」と思ったほうがわかりやすい
- 例
    - [[Oscillator Sync]] は鳴らせない（基本的には）
    - FM音源について、YAMAHA方式のphase modulationでfeedbackのあるいわゆるFM音源は、鳴らせない（基本的には）
        - WebAudio組み込みのDSPを使って実現できるのは、
            - FM元祖 John Chowning 方式 までである
                - 参考 : [[FM音源 YAMAHA方式と John Chowning 方式の違い]]
- どうしてもTone.jsでDSPを書きたい場合
    - 仮説
        - ※あくまで仮説なので注意。未検証
        - トリガーだけTone.jsにする
            - 問題
                - Tone.jsの便利なAudio Graph wrap構造は、使えない
                    - WebAudio低レイヤーのAudio Graphを自分で使うしかない
                        - よって、WebAudio低レイヤーで自作するのと大差ない、大規模な開発コストが必要になる
                            - それならWebAudio低レイヤーですべて自作するほうがスムーズかもしれない
    - non-realtimeでプリレンダリングして鳴らす
        - 問題
            - realtimeならではのインタラクティブなサウンド変化を得られない
## 注意
- リファレンスは散在しており、それぞれの妥当性は未確認
    - 情報が錯綜しており注意
