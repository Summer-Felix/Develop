# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [compile()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

compile(source, filename, mode, flags=0, dont_inherit=False, optimize=-1)

将source编译成代码对象，或者AST（Abstract Syntax Tree，抽象语法树）对象。
代码对象可以由
[exec()](http://python.usyiyi.cn/translate/python_352/library/functions.html)
或
[eval()](http://python.usyiyi.cn/translate/python_352/library/functions.html)
执行。源可以是普通字符串，字节字符串或AST对象。
有关如何使用AST对象的信息，请参阅 [ast](http://python.usyiyi.cn/translate/python_352/library/ast.html#module-ast) 模块文档。

filename参数是要从中读取代码的文件名；如果它不是从文件中读取的话，需要传入一些可识别的内容（通常使用'string'）

mode 参数指定必须编译模式；如果source由语句序列组成，则它可以是'exec'；
如果它是单个语句，则可以使用'eval'；如果它由单个交互式语句组成，则可以使用'single'。
（在最后一种情况下，非None语句将会被打印出来）

可选参数flags和dont_inherit控制哪些未来版本的语句
（见 [PEP 236](https://www.python.org/dev/peps/pep-0236/)）
会应用于源编译。如果两者都不存在（或两者都为零），则使用在调
用 [compile()](http://python.usyiyi.cn/translate/python_352/library/functions.html) 的
代码中生效的未来语句来编译代码。
如果给出了flags参数且没有给出dont_inherit参数（或者为0），
除了本该使用的future语句之外，由flags参数指明的future语句也会影响编译。
如果dont_inherit是非0整数，flags参数被忽略（调用compile周围的有效的future语句被忽略）。

future语句由bit位指明，这些bit可以做或运算，以指明多个语句。可以在[\_\_future\_\_](http://python.usyiyi.cn/translate/python_352/library/__future__.html#module-__future__)模块中，_Feature实例的compiler_flag属性找到指明功能的bit位。

参数optimize指定编译器的优化级别；默认值-1选择由-O选项给出的解释器的优化级别。显式级别为0（无优化； __debug__为真），1（声明被删除，__debug__为假 ）或2（docstrings也被删除）。

如果源包含空字节，则此函数引发 [SyntaxError](http://python.usyiyi.cn/translate/python_352/library/exceptions.html#SyntaxError)（如果编译的源无效）和 [ValueError](http://python.usyiyi.cn/translate/python_352/library/exceptions.html#ValueError)

如果要将Python代码解析为其AST表示形式，请参阅 [ast.parse()](http://python.usyiyi.cn/translate/python_352/library/ast.html#ast.parse)。

> 注意当以'single'或者'eval'模式编译多行代码字符串的时候，输入至少以一个新行结尾。这主要是便
于 [code](http://python.usyiyi.cn/translate/python_352/library/code.html#module-code) 模块检测语句是否结束。

> 改变于版本 2.3：添加了flags和dont_inherit参数。

> 改变于版本2.6：支持编译AST对象。

> 改变于版本2.7：允许使用Windows和Mac的新行字符。'exec'模式下的输入不需要以新行结束。

> 在版本3.2中已更改：允许使用Windows和Mac换行符。还在'exec'模式中输入不必在换行符中结束。添加了optimize参数。

> 在版本3.5中更改：以前，在source中遇到空字节时引发 [TypeError](http://python.usyiyi.cn/translate/python_352/library/exceptions.html#TypeError)。
