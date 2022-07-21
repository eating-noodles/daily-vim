# 掌握宏
## 宏
可以录制一系列动作。可以理解为函数，预先定义一系列的vim命令来实现某个功能，当需要这个功能时，直接调用宏即可。

## 录制宏
* 命令：`q` + 寄存器的名称a(a就是把命令保存在哪里,可以理解为方法名称)
* 输入qa以后,就开始了宏的录制

## 录制过程tips
* 录制的时候，先规范好光标的位置
  * 比如，先输入`0`将光标置于行首
* 移动光标的时候使用相对位置
  * `w`,`e`,`textObject`,`f`,`t`这些都可以算是相对位置
  * `hjkl` 这些算是绝对位置
  * e.g.
    假设我现在有如下文本：
    ``` javascript
      1. a;
      2. b;
      10. c;
    ```
    光标在行首，希望将光标移动到`.`的位置并删除掉`.`，如果使用`l`，对于前两行1和2是可以的，但是对于第三行的10，需要向右移动两次才可以，这样的话，录制的宏作用在第三行时，就会出错。
    如果使用`w`，不管序号有多长，一次通用的`w`操作就可以。

## 结束录制
* 再次输入`q`就会退出宏的录制

## 查看录制好的宏
* 命令：`:reg ` + a(寄存器的名称)
* 输入`:reg a`,可以看到宏a包含了那些vim操作

## 使用宏
* 根据名称使用宏
  * 命令：`@` + 宏名称
  * e.g. `@a`
* 使用上一次的宏
  * 命令：`@@`
* 重复使用某个宏
  * 命令：次数 + `@` + 宏名称
  * e.g. `3@a` 调用3次名称为a的宏

## 修改宏
### 追加
* 命令：`q` + 宏名称的大写
  * e.g. `qA` 
    * 假设已经有一个宏a,输入qA就可以修改a的内容，修改方式是在a已有的内容后面进行追加。
    * 再输入q，就会退出修改
### 修改一个已知的宏
* 取出寄存器的内容
  * 方式1：`"` + 寄存器的名称 + `p`
    * e.g. `"ap`
  * 方式2：`:put ` + 寄存器名称

* 修改寄存器的内容

* 将修改后的内容同步到寄存器(vscode的vim插件有bug不支持这种方式,终端支持)
  * 方式1：`"` + 寄存器的名称 + `yw`
    * e.g. `"ayw`
  * 方式2：`"` + 寄存器的名称 + `yy`
    * e.g. `"ayy`

## 其他
### 安全机制
报错就会停止执行


## practice
1. a;
2. b;
10. c;