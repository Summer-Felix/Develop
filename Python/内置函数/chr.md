# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [chr()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

chr(i)

返回表示 Unicode 码点为整数i的字符的字符串。

例如，chr(97)返回字符串'a'，而chr(8364)返回字符串'€'它
是 [ord()](http://python.usyiyi.cn/translate/python_352/library/functions.html) 的逆操作。

参数的有效范围为0到1,114,111（基址16中的0x10FFFF）。
如果i超出该范围，则会引发 [ValueError](http://python.usyiyi.cn/translate/python_352/library/exceptions.html#ValueError)。
