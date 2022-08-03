# 掌握重构
## vscode
### 重构提示
* `commnad + .`
* `ctrl + shift + r`

### 文档
* code.visualstudio.com/docs/typescript/typescript-refactoring

### 提炼函数
* 功能：将选中的代码提取到一个新的函数中
* 使用
  * 选中要操作的代码
  * `ctrl + shift + r` windows; `command + .` macos
  * 选择提取内容到函数

### 提炼变量
* 功能：假如有`console.log('aaaa')`代码，想要将aaaa提炼成一个变量
* 使用
  * 选中想要操作的代码
  * `ctrl + shift + r` windows; `command + .` macos
  * 选择对应的选项

## 重构插件 增强vscode重构功能
### Abracadabra
* 文档： 见github

#### 内联变量
* 功能： 和提炼变量功能相反


### hocus pocus
* 代码中有语法错误时，此插件会不生效

#### 创建function


#### 创建变量
* 功能：代码中使用了某个变量，但是还没创建，可以使用此插件进行创建
* 改键： setting.json
``` json
"vim.normalModeKeyBindingsNonRecursive": [
  {
    "before": ["<Leader>", "f", "f"],
    "commands": ["hocusPocus.createFunction"]
  },
  {
    "before": ["<Leader>", "v", "v"],
    "commands": ["hocusPocus.createVariable"]
  },
]
```

### javascript booster
