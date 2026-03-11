# これはなに？
- [[Obsidian]] + [[Quartz 4]] 向けのプラグインのexamplesです。
    - コード進行を五線譜で表示して、
        - クリックで演奏できます。
    - Obsidianに `Dm7` などを書くだけでOK
        - あとはObsidianプラグインとQuartz 4プラグインが五線譜にして演奏してくれます

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

# 実現方法
- [[Quartz 4]]拡張機能を、[[Coding Agent]] に生成させた
    - [[quartz-transformer-mmlabc]]
