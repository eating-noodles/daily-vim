# 处理包裹字符的符号
## vim-surround
1. 替换已有字符的符号
* 语法
c(change) + s(surround) + 目标符号 + 想要替换的符号

* 举例
比如，我现在有
``` javascript
const a = "b${name}";
```
想把双引号替换为反引号(``)
将光标移动到文本上,然后输入 cs"` 就可以了，结果为:
``` javascript
const a = `b${name}`;
```

2. 添加
* 语法
y + s(surround) + motion(范围) + 想要的符号

* 举例
我现在有
``` javascript
import add from './add';
```
我想给add添加花括号
输入 ```ys iw {```就可以了,结果为:
``` javascript
import { add } from './add';
```

3. 删除
* 语法
d + s + 想删除的符号

* 举例
我现在有
``` javascript
import { add } from  "./add";
```
我想删除add的花括号
输入 ```ds {```就可以了,结果为:
``` javascript
import add from "./add";
```

4. 可视化模式下使用
* 语法
范围 + S + 想添加的符号
