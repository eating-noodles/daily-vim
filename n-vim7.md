# 在文件中移动的更快
1. 滚动
* ctrl - f forward 向下滚动一屏幕
* ctrl - b backward 向上滚动一屏幕
* ctrl - d 向上滚动半屏幕
* ctrl - u 向上滚动半屏幕
* ctrl - y 向上滚动一行
* ctrl - e 向下滚动一行
2. 基于配置做滚动
* shift + j 向下滚动5行
* shift + k 向上滚动5行
vscode配置 setting.json
``` json
  "vim.visualModeKeyBindings": [
    {
      "before": ["J"],
      "after": [
        "5",
        "j"
      ],
    },
    {
      "before": ["K"],
      "after": [
        "5",
        "k"
      ],
    },
  ],
  "vim.normalModeKeyBindings": [
    {
      "before": ["J"],
      "after": [
        "5",
        "j"
      ],
    },
    {
      "before": ["K"],
      "after": [
        "5",
        "k"
      ],
    },
  ],
```
3. zz 将当前行置于屏幕中央
4. zt 将当前行置于屏幕最上方
5. zb 将当前行置于屏幕最下方
6. gg 跳到文件首部
7. G 跳到文件底部
8. 行号 + gg/G  跳转到指定行
