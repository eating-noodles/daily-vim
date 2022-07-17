# 更有效率的处理单字符
1. x 删除当前光标所在的字符(重要) X 删除当前光标的前一个字符
2. s 删除当前光标的字符 并进入insert模式(重要) S 删除当前光标所在行并进入insert模式(重要)
3. r 替换一个字符(重要) e.g. r2 将当前光标所在的字符替换为2;
R 替换多个字符 从当前光标开始进行替换
4. u 撤销刚才的操作
   ctrl-r redo
* 从进入insert模式开始到进入normal模式 叫做一个可撤销块。方向键上下左右会影响形成可撤销块。








# 练习
``` javascript
function tastFor() {
  const obj = {}
  const a = 1
  const b = 2
  one two aaa
}
```
