# 文本对象
1. 定义
文档中的一个单词，一对标点符号，一个代码块等等都可以叫做一个文本对象。文本对象可以快速选择。文本对象表示一个范围。
2. 语法
* operator + i(内部) / a(外部) + 文本对象(范围)
* 可视化模式 + i / a + 文本对象 + operator
3. 内部 / 外部
* i 内部
  * 对于()这个文本对象，i会选中括号内部的东西

* a 外部
  * 对于()这个文本对象，a会选中括号内部的东西 + 括号本身

4. 对象
* w 单词
  * 内部 i: 选中当前整个单词
  * 外部 a: 
    * 单词前、后面有空格时, 选中整个单词+后面的空格
    * 单词前面有空格、后面没有时, 选中整个单词+前面的空格
* b 表示一对()
* B 表示一对{}
* <>、[]、{}、''、"" 等用法同()
* t 可以选择xml标签中的内容
* s 表示句子（以 . ! ? 结尾的叫句子）
* p 表示段落 空格间隔开的块
5. vscode集成的内部对象
* a 方法参数对象(arguments)
  * cia 删除某个参数并编辑
  * daa 删除某个参数和逗号
* e 文件对象(entire)
  * die 删除整个文件的内容 不包括文件首尾的空格
  * dae 删除整个文件的内容 包含首尾空格








# practice
``` javascript
function name(params) {
  console.log('[aaaaa]')
}

```