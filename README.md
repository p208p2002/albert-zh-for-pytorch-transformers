# Albert-zh for pytorch-transformers
- 僅僅是基於**參考**進行轉換而已
- Albert zh for [pytorch-transformers](https://github.com/huggingface/transformers)
- 測試支援繁體中文
- 轉換好的模型請見[release](https://github.com/p208p2002/albert-zh-convert-testing/releases)
- 用法參見`test.py`

## 可用模型 
- albert_tiny_zh
- albert_base_zh
- albert_large_zh
- albert_xlarge_zh

## 問題
可能會遭遇到訓練時模型亂印東西。請用`log()`代替`print()`，並且在程式開始的時候先執行一次`blockPrint()`
```python
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

## 測試環境
- python 3.6.4
- pyotrch 1.3 (with cuda 10)
- transformers 2.2.2

## 參考
### albert zh
- https://github.com/brightmart/albert_zh
### albert tf to pytorch
- https://github.com/lonePatient/albert_pytorch
