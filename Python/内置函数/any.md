# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [any()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

any(iterable)
如果iterable里任何一个元素为True，返回 True。如果iterable为空（empty）,返回 False。

等同于：

```
def any(iterable):
    for element in iterable:
        if element:
            return True
    return False
```

> 添加于版本2.5。
