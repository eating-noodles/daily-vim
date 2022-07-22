# vim调用vscode命令

## commands字段
* 可以在`setting.json`文件中做键位映射
* 格式
``` json
{
    "before": [],
    "command": []
}
``` 
* commands字段有两种格式，一种可以填写字符串，内容为vscode定义的命令简称；第二种可以填写命令对象，包含命令名称和命令的参数。

## 示例
### 重命名
1. 查看vscode的命令
* `ctrl + shift + p`打开vscode的`Keyboard Shortcuts`文件进行查看。
* 文件中展示的`commands`列即为命令的简称；右键复制，复制的内容为此命令对象的详细信息。
    * e.g.
    ``` json
    {
        "key": "f2",
        "command": "editor.action.rename",
        "when": "editorHasRenameProvider && editorTextFocus && !editorReadonly"
    }
    ```
* 可以看出vscode中的命令为`f2`

2. 做键位映射
* 在`setting.json`中设置相应的映射
``` json
"vim.normalModeKeyBindingsNonRecursive": [
    {
        "before": ["<Leader>", "r", "n"],
        "commands": ["editor.action.rename"]
    }
]
```
### 格式化代码
操作步骤同上，最终的键位映射为：
``` json
"vim.normalModeKeyBindingsNonRecursive": [
    {
        "before": ["<Leader>", "f", "d"],
        "commands": ["editor.action.formatDocument"]
    }
]
```
### 折叠打开代码
操作步骤同上，最终键位映射为,这里需要注意的是commands可以组合命令：
``` json
"vim.normalModeKeyBindingsNonRecursive": [
    {
        "before": ["<Leader>", "["],
        "commands": [
          {
            "command": "editor.fold",
          },
          {
            "command": "vim.remap",
            "args": {
              "after": ["$", "%"],
            }
          }
        ]
    },
    {
        "before": ["<Leader>", "]"],
        "commands": [
          {
            "command": "editor.unfold",
          },
        ]
    }

]
```
