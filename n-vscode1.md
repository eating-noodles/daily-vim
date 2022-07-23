# 操作文件
## 文件区域的切换
### 切换到文件资源管理器
1. vim
* 之前课程配置：`shift + 方向键`
* 局限是，只有vim命令生效的地方可以使用。如果在终端中输入切换会不起作用。

2. vscode
* `Keyboard Shortcuts`中切换到文件资源管理器的默认命令为`shift + command + E`
* 修改键位为：`ctrl+;`
* 编辑区时，按下`ctrl+;`会切换到文件资源管理器；在资源管理器区域时，按下`ctrl+;`会切换到编辑区。
``` json
{
  "key": "ctrl+;",
  "command": "workbench.view.explorer",
  "when": "viewcontainer.workbench.view.explorer.enabled"
}
```

### 切换到编辑区域
* vscode默认的切换到编辑区域的键位是`command+1`
* 我们修改键位为：`ctrl+'`
``` json
{
  "key": "ctrl+'",
  "command": "workbench.action.focusFirstEditorGroup"
}
```
## 资源管理器的操作
### 移动光标
* 使用`jk`即可

### 折叠展开
* 使用`hl`即可

### 创建文件
1. 光标在资源管理器时
* 使用`a`即可,配置键位 keybindings.json
``` json
{
  "key": "a",
  "command": "explorer.newFile",
  "when": "filesExplorerFocus && !inputFocus"
}
```
2. 光标在编辑区域，想在当前文件同级创建文件
* 使用`<Leader> + n + f`即可,改键 setting.json
``` json
"vim.normalModeKeyBindingsNonRecursive": [
  {
    "before": ["<Leader>", "n", "f"],
    "commands":["explorer.newFile"],
  },
]
```
3. vscode自带的命令
* command + n, 但是需要手动指定保存位置

4. 使用vscode插件 file utils

### 创建文件夹
1. 光标在资源管理器时
* 使用`A`即可,配置键位 keybindings.json
``` json
{
  "key": "shift+a",
  "command": "explorer.newFolder",
  "when": "filesExplorerFocus && !inputFocus"
}
```
2. 光标在编辑区域，想在当前文件同级创建文件
* 使用`<Leader> + n + d`即可,改键 setting.json
``` json
"vim.normalModeKeyBindingsNonRecursive": [
  {
    "before": ["<Leader>", "n", "d"],
    "commands":["explorer.newFolder"],
  },
]
```
3. 使用vscode插件 file utils

### 重命名
* 使用`r`来重命名 keybindings.json
``` json
{
  "key": "r",
  "command": "renameFile",
  "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
}
```

### 删除
* 使用`d`来重命名 keybindings.json
``` json
{
  "key": "d",
  "command": "deleteFile",
  "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceReadonly && !inputFocus"
}
```


