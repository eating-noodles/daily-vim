# 编码中的常用快捷键

## 展示当前可使用项 show code action
`command + .`

## 触发函数的参数提醒
* 一般是在insert模式使用，normal模式也可用
* `shift + command + space`
* 通常是使用某个定义好的函数时，手动去触发参数提醒

## 手动触发建议
* 一般是在insert模式使用，normal模式也可用
* `command + i`
* 手动触发代码建议

## 移动整行代码
* normal模式和insert模式下均可使用
* `opt + up/down` (macOs)
* `alt + up/down` (windows)

## 增加一个空行
* normal模式和insert模式下均可使用
* 在某行下方
  * `command + enter`
  * 光标在行内任意位置的时候，可以通过这个快捷键来增加一个空行
* 在某行上方
  * `command + shift + enter`

## 删除光标前面的单词
* normal模式和insert模式下均可使用
* 在某行下方
* `opt + delete`
  * 对于`getName`,会将整个`getName`删除
* `opt + ctrl + delete`
  * 对于`getName`,光标在结尾时，输入一遍此命令，会将`Name`删除，留下`get`

## 跳转到代码错误处（一般是代码中标红的位置）
* `f8`
* 返回到上一个报错的地方：`shift + f8`

## 选择所有出现的当前单词
* normal模式和insert模式下均可使用
* `command + f2`
