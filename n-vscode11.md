# 终端(macOS)
keybindings.json
## 打开终端
* ``ctrl + `(反引号)``
* 可以改键，对应：workbench.action.terminal.toggleTerminal
* `cmd + j`

## 清空
* `cmd + k`

## 分屏
* `cmd + \`
* "command": "workbench.action.terminal.split"

## 分屏切换
* 改键：`cmd + [`  `cmd + ]`
* workbench.action.terminal.focusNextPanel
* workbench.action.terminal.focusPreviousPanel

## 关闭
* `shift + alt + q`
* workbench.action.terminal.kill

## 新建
* `shift + alt + n`
* workbench.action.terminal.new

## 窗口切换
* `shift + cmd + [` `shift + cmd + ]`

## 直接打开终端
* `shift + cmd + c`
* 修改默认打开的终端： setting.json
``` json
"terminal.external.osxExec": "iTerm.app", // macOS
"terminal.external.windowsExec": "", // windows
```
