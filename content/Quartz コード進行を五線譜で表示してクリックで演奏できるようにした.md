# examples
## コード進行
```chord
C
```


## MML
```mml
c
```


## ABC
```abc
C
```

# 方法
- Quartz拡張機能を、coding agentに生成させた
    - [[quartz-transformer-mmlabc]]
# 状況
- 落ちたり
- スーパーリロードでなおったり
- スーパーリロードでもなおらなかったり
- 様子見中、調査中
- もし埒が明かないなら、動いていた（だが表示されないことがありリロードでなおった）段階に切り戻してから再検討します
- 埒が明かないので切り戻して調査中です
- 切り戻し
    - 切り戻しても「リロードでなおらない」状態になりました
- 分析
    - coding agentが生成したoctave逆の`>` について、userが`<`にしたので、そのときに潜在バグが顕在化した可能性があるのでそこを切り分け調査します
- 結果
    - 変わらず
    - `Quartz-コード進行を五線譜で表示してクリックで演奏できるようにした:271 Uncaught SyntaxError: Unexpected token '>' (at Quartz-コード進行を五線譜で表示してクリックで演奏できるようにした:271:28)`
    - 切り戻し、さらにoctave MMLを外したにも関わらずエラーになっています
- 切り分け
    - 1文字のMMLやchordにします
    - `backup : C Dm7 G7^2, CM7`
    - `backup : t120 l4 cdefgab`
    - backup:
```
X:1
T:ABC notation
M:4/4
L:1/4
K:C
C D E F|G A B c|
```
- 結果
    - 変わらず
- DevToolsで当該codeまで追いかけて気付いた。`<void>`がいる。TypeScript codeである
    - そこを軸にagentに調査するよう投げた
