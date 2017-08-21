# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [delattr()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

delattr(object, name)

这个函数和 [setattr()](http://python.usyiyi.cn/translate/python_352/library/functions.html) 有关。参数是一个对象和一个字符串。字符串必须是对象的某个属性的名字。
只要对象允许，这个函数删除该名字对应的属性。例如，delattr(x, 'foobar')等同于del x.foobar。

```
class dict(**kwarg)
class dict(mapping, **kwarg)
class dict(iterable, **kwarg)
```

创建一个新字典。[dict](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#dict) 对象是字典类。有关此类的文档，请参见dict和[映射类型 - dict](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#typesmapping)。

> 对于其他容器，请参阅内置的[列表](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#list)，[集合](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#set)和[元组](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#tuple)类以及[容器](http://python.usyiyi.cn/translate/python_352/library/collections.html#module-collections) 。
