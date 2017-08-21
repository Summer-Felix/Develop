# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [classmethod()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

classmethod(function)

将函数包装成类方法。

类方法接受类作为隐式的第一个参数，就像实例方法接受实例作为隐式的第一个参数一样。
声明一个类方法，使用这样的惯例：

```
class C:
    @classmethod
    def f(cls, arg1, arg2, ...): ...
```

@classmethod形式是一个函数[装饰器](http://python.usyiyi.cn/translate/python_352/glossary.html#term-decorator) —— 查看
[函数定义](http://python.usyiyi.cn/translate/python_352/reference/compound_stmts.html#function)
中关于函数定义的详细说明。

它既可以在类上调用（如C.f()）也可以在实例上调用（如C().f()）。除了实例的类，实例本身被忽略。
如果一个类方法在子类上调用，那么子类对象被传递为隐式的第一个参数。

类方法不同于C++或Java中的静态方法。如果你需要静态方法，参见本节中的 [staticmethod()](http://python.usyiyi.cn/translate/python_352/library/functions.html)。

关于类方法更多的信息，参考
[标注类型的层级](http://python.usyiyi.cn/translate/python_352/reference/datamodel.html#types)
中的标准类型层级的文档。

> 版本 2.2 新增。

> 改变于版本2.4：添加了函数装饰器语法。
