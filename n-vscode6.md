# 搞定git
## 显示source control面板
* `<Leader> g g`
* vscode内置的可以看到文件状态的面板
* 改键位： setting.json
``` json
"vim.normalModeKeyBindingsNonRecursive": [
  {
    "before": ["<Leader>", "g", "g"],
    "commands": ["workbench.view.scm"]
  }
]
```

## stage change
* `<Leader> g s`
* git add + path
* 改键位 setting.json
``` json
"vim.normalModeKeyBindingsNonRecursive": [
  {
    "before": ["<Leader>", "g", "s"],
    "commands": ["git.stage"]
  }
]
```

## commit
* `<Leader> g c`
* 改键位 setting.json
``` json
"vim.normalModeKeyBindingsNonRecursive": [
  {
    "before": ["<Leader>", "g", "c"],
    "commands": ["git.commit"]
  }
]
```

## diff
* `<Leader> g d f`
* 改键位 setting.json
``` json
"vim.normalModeKeyBindingsNonRecursive": [
  {
    "before": ["<Leader>", "g", "d", "f"],
    "commands": ["git.openChange"]
  }
]
```

## unstage change
* `<Leader> g u`
* 取消git add
* 改键位 setting.json
``` json
"vim.normalModeKeyBindingsNonRecursive": [
  {
    "before": ["<Leader>", "g", "u"],
    "commands": ["git.unstage"]
  }
]
```

## discard change
* `<Leader> g c l`
* 类似于`git checkout + path`
* 改键位 setting.json
``` json
"vim.normalModeKeyBindingsNonRecursive": [
  {
    "before": ["<Leader>", "g", "c", "l"],
    "commands": ["git.clean"]
  }
]
```

## edamagit 插件
