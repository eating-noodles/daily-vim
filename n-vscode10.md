# VSpaceCode(whichkey)插件介绍
## 文档 
* https://vspacecode.github.io/docs/
## 初始化
* setting.json
``` json
"vim.normalModeKeyBindingsNonRecursive": [
  {
    "before": ["space",  ";"],
    "commands": ["vspacecode.space"]
  }
]
```

* keybindings.json
``` json 
  [
    // Trigger vspacecode in empty editor group
    {
        "key": "space",
        "command": "vspacecode.space",
        "when": "activeEditorGroupEmpty && focusedView == '' && !whichkeyActive && !inputFocus"
    },
    // Trigger vspacecode when sidebar is in focus
    {
        "key": "space",
        "command": "vspacecode.space",
        "when": "sideBarFocus && !inputFocus && !whichkeyActive"
    },
  ]
```
* 快速移动的配置 keybinding.json
``` json
[
      // Easy navigation in quick open/QuickPick
    {
        "key": "ctrl+j",
        "command": "workbench.action.quickOpenSelectNext",
        "when": "inQuickOpen"
    },
    {
        "key": "ctrl+k",
        "command": "workbench.action.quickOpenSelectPrevious",
        "when": "inQuickOpen"
    },
    // Easy navigation in suggestion/intellisense
    // Cannot be added to package.json because of conflict with vim's default bindings
    {
        "key": "ctrl+j",
        "command": "selectNextSuggestion",
        "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
    },
    {
        "key": "ctrl+k",
        "command": "selectPrevSuggestion",
        "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
    },
    {
        "key": "ctrl+l",
        "command": "acceptSelectedSuggestion",
        "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
    },
    // Easy navigation in parameter hint (i.e. traverse the hints when there's multiple overload for one method)
    // Cannot be added to package.json because of conflict with vim's default bindings
    {
        "key": "ctrl+j",
        "command": "showNextParameterHint",
        "when": "editorFocus && parameterHintsMultipleSignatures && parameterHintsVisible"
    },
    {
        "key": "ctrl+k",
        "command": "showPrevParameterHint",
        "when": "editorFocus && parameterHintsMultipleSignatures && parameterHintsVisible"
    },
    // Add ctrl+h/l to navigate in file browser
    {
        "key": "ctrl+h",
        "command": "file-browser.stepOut",
        "when": "inFileBrowser"
    },
    {
        "key": "ctrl+l",
        "command": "file-browser.stepIn",
        "when": "inFileBrowser"
    }
]
```

## 在原有的键位上进行修改
### 修改 
* setting.json
``` json
"vspacecode.bindingOverrides": [
  {
    "keys": "g.s",
    "name": "Go to line",
    "type": "command",
    "command": "workbench.action.gotoLine"
  }
]
```
* 覆盖`g.s`默认的行为，修改为"go to line"

### 新增
* 直接在`setting.json`文件中新增即可

### 删除已有的命令
* 把"position"的值修改为-1即可
* setting.json
``` json
"vspacecode.bindingOverrides": [
  {
    "keys": "g.s",
    // "keys": [ "g","s" ],
    "position": -1
  }
]
```

### 重写
* setting.json
``` json
"vspacecode.bindingOverrides": [
  {
    "keys": "g",
    "name": "Go...",
    "type": "bindings",
    "bindings": [
      {
        "key": "s",
        "name": "Go to line",
        "type": "command",
        "command": "workbench.action.gotoLine"
      }
    ]
  }
]
```
* "type"要设置为"bindings"

## 完全自定义
* setting.json
``` json
"vspacecode.bindings": [
  // 内容同`重写`, bindings数组中的对象是key 不是keys 
  {
    "keys": "g",
    "name": "Go...",
    "type": "bindings",
    "bindings": [
      {
        "key": "s",
        "name": "Go to line",
        "type": "command",
        "command": "workbench.action.gotoLine"
      }
    ]
  }
]
```

## 可以将vspacecode和vim快捷键结合
* 可参考文档：https://github.com/VSpaceCode/VSpaceCode/blob/vscode-vim/settings.json
