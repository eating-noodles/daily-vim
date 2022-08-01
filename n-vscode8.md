# snippets 代码片段

## 插件
1. javascript(es6) code snippets
2. vue 3 snippets
3. vue vscode snippets


## 常用

### imp
* javascript code snippets
* `import xxx from xxx;`

### imd
* javascript code snippets
* `import { xxx } from xxx;`

### fn
* 定义函数 `function xxx() {}`

### log
* `console.log(xxx)`

### vue

### anfn
* 箭头函数

### iife
* 立即执行函数

### rp
* `return new Promise()...`

## 技巧
1. tab键可以切换位置
2. 如果不小心提示消失，可以用
  * command + i
  * ctrl + space

## 拓展(自己实现一个snippet)
### 文档
* code.visualstudio.com/docs/editor/userdefinedsnippets
* snippet-generator.app 自动生成snippet模板的工具

### 创建
1. 打开vscode命令栏 输入`> configure user snippets` 
2. （作用域：）选择`new global snippet file...` 这样创建的是全局的代码片段
  * 也可以输入/选择某个语言，创建语言对应的代码片段
  * 也可以选择项目，基于项目来创建代码片段
3. 然后vscode会根据输入的名称，生成一个`xxx.code-snippets`的json文件
4. 对象分析：
``` json
	"Print to console": {
		"scope": "javascript,typescript",
		"prefix": "log",
		"body": [
			"console.log('$1');",
			"$2"
		],
		"description": "Log output to console"
	}
```
  * "Print to console"是snippet的名称,使用的时候可以看到
  * scope: 代码片段生效的作用域，示例中表示这个代码片段只会在js和ts中生效
  * prefix: 使用的时候，输入什么会生效出现
  * body: 完整的代码片段是什么
    * body中的$1、$2是当我们生成代码后，按下`tab`的时候，光标跳转的地方，叫tap stop
  * description: 描述这个代码片段是干什么的
5. 一些语法：
  * 在body里面指定默认值的语法
  ``` json
      ...,
      "body": [
        "console.log('${1:这是默认值}');",
        "$2"
      ],
      ...
  ```
  * 指定多选
  ``` json
      "body": [
        "console.${2|log,debug,error|}('${1:这是默认值}');",
        "$3"
      ],
  ```
  用户使用的时候，对于第二个参数，可以选择使用log、debug还是error
  * 支持vscode内部变量
  ``` json
      "body": [
        "console.log('${1:$TM_FILENAME}');",
        "$2"
      ],
  ```
  `$TM_FILENAME`是vscode内部变量，标识当前文件名称
