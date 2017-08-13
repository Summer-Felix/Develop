# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [all()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

all(iterable)
如果iterable的所有元素为真（或者iterable为空）， 返回True。等同于：

```
def all(iterable):
  for element in iterable:
    if not element:
      return False
    return True
```

> 添加于版本2.5。
