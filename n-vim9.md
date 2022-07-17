# 更高效的移动
## vim-easymotion
1. 开启使用：vscode setting.json
``` json
" vim-easymotion": true
```
2. vim - <leader>键
* 默认为 反斜杠键
* 修改为 空格键
``` json
"vim.leader": "<Space>",
```
3. 基于单词(常用):
光标以下的位置:
* <leader><leader>w
输入以后，光标以下的单词开头会标红，再次输入任意标红的字母，可以跳转到标红字母的位置(word)
* <leader><leader>e
和上面的命令对应，标红字母在单词尾部，可以跳转到标红字母的位置（end）

光标以上的位置:
* <leader><leader>b
输入以后,光标以上的单词开头会标红
* <leader><leader>ge
输入以后,光标以上的单词结尾会标红

4. 基于行：
* <leader><leader>j
输入以后，光标以下每行首字符会标红，输入跳转
* <leader><leader>k
输入以后，光标以上每行首字符会标红，输入跳转

5. 更详细的跳转位置
光标以下的位置:
* <leader><leader>l
和<leader><leader>w作用相似，但是可跳转位置更多
光标以上的位置:
* <leader><leader>h

* <leader><leader><leader>j 光标上下都显示

## vim-snake
1. 开启使用：vscode setting.json
``` json
" vim-sneak": true
```
2. 使用
* s + 两个字符
使用两个字符进行搜索，按;(分号)跳转下一个  按,(逗号)跳转上一个
* S + 两个字符
和`s`类似，搜索方向相反，为向上搜索

3. 改键
* 使用sneak来替换原生的f按键, 并且恢复s键原生功能
* 可视化模式下,不支持sneak的F操作
* operationpending模式下,是z键操作，不是s键，我们也将其修改为f键
``` json
  "vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": [
        "f"
      ],
      "after": [
        "s"
      ],
    },
    {
      "before": [
        "F"
      ],
      "after": [
        "S"
      ],
    },
    {
      "before": [
        "s"
      ],
      "after": [
        "c",
        "l"
      ],
    },
    {
      "before": [
        "S"
      ],
      "after": [
        "^",
        "C"
      ],
    },
  ],
  "vim.visualModeKeyBindingsNonRecursive": [
    {
      "before": [
        "f"
      ],
      "after": [
        "s"
      ],
    },
  ],
  "vim.operatorPendingModeKeyBindingsNonRecursive": [
    {
      "before": [
        "f"
      ],
      "after": [
        "z"
      ],
    },
    {
      "before": [
        "F"
      ],
      "after": [
        "Z"
      ],
    },
  ]
```

