# 页面内的操作
## 进入文本框选择模式
* `gi`
* 聚焦搜索框

## 复制当前标签页
* `yy` 会将当前页面的地址复制到系统的剪切板
* 先`yy` 再`P`会新建一个tab页打开当前页面地址;`p`会将当前页面地址替换为复制的地址

## 关闭当前标签页
* `x`
* chrome自带的键位：`command + w`

## 刷新页面
* `r`
* chrome自带的键位：`command + r`

## 选择文字
* 进入可视化模式`yv`
* 进入可视化行模式`V`
* 然后可以试用`jkhl`进行文字选择，按`command c、v`进行复制粘贴

## 改键
* 文档：https://github.com/gdh1995/vimium-c/wiki/Use-in-another-keyboard-layout
* 插件的设置页面： 自定义快捷键
``` json
mapKey <L:v> <$>
mapKey <H:v> <0>
```
`<L:v><$>`的意思是把`L`键映射为`$`，并且只在`v`模式（可视化模式）下生效.
