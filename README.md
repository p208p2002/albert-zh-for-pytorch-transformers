
# Albert zh 轉換測試
- 僅僅是基於"參考"進行轉換而已
- Albert zh for pytorch-transformers
- 測試支援繁體中文
- 轉換好的模型請見[release](https://github.com/p208p2002/albert-zh-convert-testing/releases)

## 問題
可能會遭遇到訓練時模型亂印東西，用請用log代替print
```
import os,sys
def log(*logs):
    enablePrint()
    print(*logs)
    blockPrint()

# Disable
def blockPrint():
    sys.stdout = open(os.devnull, 'w')

# Restore
def enablePrint():
    sys.stdout = sys.__stdout__
```

## 參考
### albert zh
- https://github.com/brightmart/albert_zh
### albert tf to pytorch
- https://github.com/lonePatient/albert_pytorch
