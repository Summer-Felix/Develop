# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [dir()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

dir([object])

如果没有参数，返回当前本地作用域内的名字列表。如果有参数，尝试返回参数所指明对象的合法属性的列表。

如果对象具有名为[\_\_dir\_\_()](http://python.usyiyi.cn/translate/python_352/reference/datamodel.html#object.__dir__)的方法，那么将调用此方法，并且必须返回属性列表。
这允许实现自定义
[\_\_getattr\_\_()](http://python.usyiyi.cn/translate/python_352/reference/datamodel.html#object.__getattr__)
或
[\_\_getattribute\_\_()](http://python.usyiyi.cn/translate/python_352/reference/datamodel.html#object.__getattribute__)
函数的对象自定义dir()报告其属性的方式。

如果对象不提供__dir__()，则函数会尽量从对象的__dict__属性（如果已定义）和其类型对象中收集信息。
结果列表不一定是完整的，并且当对象具有自定义
[\_\_getattr\_\_()](http://python.usyiyi.cn/translate/python_352/reference/datamodel.html#object.__getattr__)
时，可能不准确。

默认的dir()机制对于不同类型的对象具有不同的行为，因为它尝试生成最相关，而不是完整的信息：

* 如果对象是模块对象，列表包含模块的属性名。
* 如果对象是类型或者类对象，列表包含类的属性名，及它的基类的属性名。
* 否则，列表包含对象的属性名，它的类的属性名和类的基类的属性名。
* 返回的列表按字母顺序排序。例如：

```
>>>
>>> import struct
>>> dir()   # show the names in the module namespace
['__builtins__', '__name__', 'struct']
>>> dir(struct)   # show the names in the struct module 
['Struct', '__all__', '__builtins__', '__cached__', '__doc__', '__file__',
 '__initializing__', '__loader__', '__name__', '__package__',
 '_clearcache', 'calcsize', 'error', 'pack', 'pack_into',
 'unpack', 'unpack_from']
>>> class Shape:
...     def __dir__(self):
...         return ['area', 'perimeter', 'location']
>>> s = Shape()
>>> dir(s)
['area', 'location', 'perimeter']
```

> 注意因为dir()主要是方便在交互式环境中使用，它尝试提供一组有用的名称，而不是试图提供完整或一致性的名称集合，具体的行为在不同的版本之间会有变化。

> 例如，如果参数是一个类，那么元类属性就不会出现在结果中。