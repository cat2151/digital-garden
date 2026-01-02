# 手順
- `pipx install git+～` で、installできる
    - 用途：
        - 環境を汚さずアプリをinstallする用
        - GitHubから楽にinstallする用
            - ※これはpip等でも可能
    - 仕組み：
        - GitHubからinstallされる
        - これを使ってinstallしたものは、
            - 実行時、
            - そのアプリのコマンドを入力するだけで、
            - 自動的に
                - そのアプリ専用の
                    - 仮想環境内で
                        - 実行されるので
                            - 環境を汚さない
## 例
```bash
# Install
pipx install git+https://github.com/cat2151/cat-oscillator-sync

# Run
cat-oscillator-sync-smooth
```
- 爆音注意
    - 起動するだけで爆音（playボタンはありません）
- 内容
    - ソフトシンセ
        - オシレータシンク音色を鳴らす簡易ソフトシンセです
# run
- `pipx run git+～` で、実行もできる
    - 用途：
        - お試し用
    - 仕組み：
        - GitHubから
        - 仮想環境を一時的に構築し
            - そこに一時的にinstallし
                - 実行
        - 実行後、仮想環境とinstallしたものは
            - 自動で消えるので
                - 環境を汚さない
## 例
```bash
pipx run --spec git+https://github.com/cat2151/cat-oscillator-sync cat-oscillator-sync-smooth
```
- 1分～数分待ってください
    - 一時的なinstall処理のためです
- 爆音注意
    - 起動するだけで爆音（playボタンはありません）
- 内容
    - ソフトシンセ
        - オシレータシンク音色を鳴らす簡易ソフトシンセです
# 公式
- [pipx](https://pipx.pypa.io/stable/)
- GitHub
    - [GitHub - pypa/pipx: Install and Run Python Applications in Isolated Environments](https://github.com/pypa/pipx)
# pipxそのものはどうやってinstallするの？
- 筆者の場合は、雑にぐぐって雑にinstallして、今まで特に困っていません。
    - 詳しくは、[[割愛]]
