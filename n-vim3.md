# 掌握vim语法
1. vim语法
  操作 + 动词范围（分界点是光标方块开头的那条线）
2. 操作
  * d 删除
  * c 删除并进入编辑模式
3. 基于单词\字串进行移动
  * e 移动到单词结尾 E 移动到字串结尾
  * w 移动到单词开头 W 移动到字串开头
  * b 移动到上一个单词的开头 B 移动到上一个字串的开头
  * ge 移动到上一个单词的结尾
4. 组合
  * cw 删除当前单词 光标需要在单词开头
  * ciw 删除当前单词
  * caw 从单词中间删除当前单词 比ciw多删除一个空格
  * ea 在当前单词结尾出添加


# 改键
```
"vim.operatorPendingModeKeyBindings": [
  {
    "before": ["H"],
    "after": ["^"]
  },
  {
    "before": ["L"],
    "after": ["g", "_"]
  }
]
```


# 练习
``` javascript
function getName(){
  const a = "hello world hh"
  return ""
}
```
