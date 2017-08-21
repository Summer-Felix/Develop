# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [callable()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

callable(object)

如果该 object是可调用的，返回 True ,否则返回 False 。
如果返回True，对其调用仍有可能失败；但是如果返回False，对object的调用总是失败。
请注意，类是可调用的（调用类将返回一个新的实例）。

如果实例的类有[__call__()](http://python.usyiyi.cn/translate/python_352/reference/datamodel.html#object.__call__)方法，则它是可调用；否则它是不可调用的。

> 在 3.2版本的更新:这个函数第一次在 Python 3.0 中被移除，在Python 3.2.中被重新启用
