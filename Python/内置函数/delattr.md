# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [delattr()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

delattr(object, name)

这个函数和 [setattr()](http://python.usyiyi.cn/translate/python_352/library/functions.html) 有关。参数是一个对象和一个字符串。字符串必须是对象的某个属性的名字。
只要对象允许，这个函数删除该名字对应的属性。例如，delattr(x, 'foobar')等同于del x.foobar。
