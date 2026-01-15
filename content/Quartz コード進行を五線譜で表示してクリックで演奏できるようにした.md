# examples
## コード進行
```chord
C Dm7 G7^2, CM7
```


## MML
```mml
t120 l4 cdefgab<c
```


## ABC
```abc
X:1
T:ABC notation
M:4/4
L:1/4
K:C
C D E F|G A B c|
```

# 方法
- Quartz拡張機能を、coding agentに生成させた
    - [[quartz-transformer-mmlabc]]
# 状況
- 不具合
    - 五線譜が表示されないことがある
    - 応急対策
        - リロードで表示される
    - 恒久対策
        - 修正中
        - logをagentに実装させた
        - logで動作確認中
            - 別のpageを開いたあと、五線譜のあるpageを開いたとき、
            - 期待値：
                - 五線譜表示関連のlogが出る
            - 実際：
                - 何もlogに出ない
        - どうする？
            - 案、現状をそのままissueに投げ、現実のURLをわたして、現実にlogを確認させ、分析させる
                - まずagentが現実を調査できるか？の確認をする、ということ
                - でagentの手に余るようなら人力でlog調査をしていく

