# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [eval()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

eval(expression, globals=None, locals=None)

参数是字符串和可选的全局变量和局部变量。
如果有全局变量，globals必须是个字典。
如果有局部变量，locals可以是任何映射类型对象。

expression参数被当作Python表达式来解析并演算（技术上来说，是个条件列表），使用globals和locals字典作为全局和局部的命名空间。
如果globals字典存在，且缺少‘__builtins__’，在expression被解析之前，当前的全局变量被拷贝进globals。
这意味着expression通常具有对标准[builtins](http://python.usyiyi.cn/translate/python_352/library/builtins.html#module-builtins)的完全访问权限，并且传播受限环境。
如果locals字典被忽略，默认是globals字典。
如果两个字典都省略，则在调用[eval()](http://python.usyiyi.cn/translate/python_352/library/functions.html)的环境中执行表达式。
返回值是被演算的表达式的结果。
语法错误报告成异常。
例子：

```
>>> x = 1
>>> eval('x+1')
2
```

此函数也可用于执行任意代码对象（例如由[compile()](http://python.usyiyi.cn/translate/python_352/library/functions.html)创建的代码对象）。
在这种情况下，传递代码对象而不是字符串。如果代码对象已使用'exec'作为mode参数编译，则[eval()](http://python.usyiyi.cn/translate/python_352/library/functions.html)的返回值将为None 。

> 提示：[exec()](http://python.usyiyi.cn/translate/python_352/library/functions.html)函数支持语句的动态执行。
[globals()](http://python.usyiyi.cn/translate/python_352/library/functions.html)和[locals()](http://python.usyiyi.cn/translate/python_352/library/functions.html)函数分别返回当前的全局和局部字典，可以用于传递给eval或[exec()](http://python.usyiyi.cn/translate/python_352/library/functions.html)。

> 请参见[ast.literal_eval()](http://python.usyiyi.cn/translate/python_352/library/ast.html#ast.literal_eval)这个函数，它可以安全地计算只包含字面值表达式的字符串。