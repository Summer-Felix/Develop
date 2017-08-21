# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [enumerate()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

enumerate(iterable, start=0)

返回一个枚举对象。

iterable 必须是一个序列、一个[迭代器](http://python.usyiyi.cn/translate/python_352/glossary.html#term-iterator)，或者其它某种支持迭代的对象。
[enumerate()](http://python.usyiyi.cn/translate/python_352/library/functions.html)返回的迭代器的[\_\_next\_\_()](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#iterator.__next__)方法返回一个元组，该元组包含一个计数（从start开始，默认为0）和迭代iterable得到的值。

```
>>>
>>> seasons = ['Spring', 'Summer', 'Fall', 'Winter']
>>> list(enumerate(seasons))
[(0, 'Spring'), (1, 'Summer'), (2, 'Fall'), (3, 'Winter')]
>>> list(enumerate(seasons, start=1))
[(1, 'Spring'), (2, 'Summer'), (3, 'Fall'), (4, 'Winter')]
```

等同于：

```
def enumerate(sequence, start=0):
    n = start
    for elem in sequence:
        yield n, elem
        n += 1
```