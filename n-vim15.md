# 掌握窗口的管理
## vim
### 新建窗口
1. 左右
* Ctrl + w + v

2. 上下
* Ctrl + w + s

### 窗口的切换
1. 切换到上下左右的窗口 
Ctrl + w + h/j/k/l

2. 窗口互换
Ctrl + w + w

### 关闭窗口
Ctrl + w + c
* 当一个窗口tab打开了多个文件时,只会关闭一个文件,窗口还在

### 保留当前窗口，关闭其他窗口
Ctrl + w + o

## 拓展 vscode自定义窗口快捷键
### 新建窗口
1. 左右
command + \

2. 上下
自定义快捷键：command + ctrl + \

### 关闭其他窗口
1. 关闭某个文件
command + w

2. 关闭整个tab内的所有文件
command + k + w

### 窗口的切换
shift + 方向键
改键： keybindings.json
``` json
[
  {
    "key": "shift+left",
    "command": "vim.remap",
    "when": "vim.mode == 'Normal'",
    "args": {
      "after": [
        "<c-w>",
        "h"
      ]
    }
  },
  {
    "key": "shift+right",
    "command": "vim.remap",
    "when": "vim.mode == 'Normal'",
    "args": {
      "after": [
        "<c-w>",
        "l"
      ]
    }
  },
  {
    "key": "shift+up",
    "command": "vim.remap",
    "when": "vim.mode == 'Normal'",
    "args": {
      "after": [
        "<c-w>",
        "k"
      ]
    }
  },
  {
    "key": "shift+down",
    "command": "vim.remap",
    "when": "vim.mode == 'Normal'",
    "args": {
      "after": [
        "<c-w>",
        "j"
      ]
    }
  },
]
```
* 如果没有将 ctrl + hjkl映射到方向键的话，可以把shift + up 改成shift + ctrl + k(其余的以此类推)
