# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [complex()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

class complex([real[, imag]])

返回值形式为real + imag * 1j的复数，或将字符串或数字转换为复数。
如果第一个参数是个字符串，它将被解释成复数，同时函数不能有第二个参数。
第二个参数不能是字符串。每个参数必须是数值类型（包括复数）。
如果省略imag，则默认为零，构造函数会像int和float一样进行转换。如果省略这两个参数，则返回0j。

> 注意当从字符串转化成复数的时候，字符串中+或者-两边不能有空白。例如，complex('1+2j')是可行的，但complex('1 + 2j')会抛出 [ValueError](http://python.usyiyi.cn/translate/python_352/library/exceptions.html#ValueError) 异常。

复数类型在[数字类型 - int，float，complex](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#typesnumeric)中描述。
