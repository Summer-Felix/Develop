# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [bytearray()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

class bytearray([source[, encoding[, errors]]])
返回一个新的字节数组。bytearray 类是一个关于整数的 mutable（可变）序列，范围为0 < = x < 256。它包含了可变序列大部分的常用方法，参见 [Mutable Sequence Types](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#typesseq-mutable)，同时也包含了bytes 类型的大部分方法，参见[Bytes 和 Bytearray 操作](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#bytes-methods)
source参数可以以不同的方式来初始化数组，它是可选的：
* 如果是个字符串 string，应该直接在参数中指定编码类型，例如：utf-8 （以及可选参数 errors）；之后 bytearray() 将使用 [str.encode()](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#str.encode)按照编码转化字符串为字节序列。
* 如果是integer，生成相应大小的数组，元素初始化为空字节。
* 如果是遵循buffer接口的对象，对象的只读buffer被用来初始化字节数组。
* 如果它是可迭代类型iterable，其整数元素的取值范围是0 <= x < 256，一般用作数组的初始内容。

如果没有参数，它创建一个大小为0的数组。

参见 [Binary Sequence Types — bytes, bytearray, memoryview](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#binaryseq) 和 [Bytearray Objects](http://python.usyiyi.cn/translate/python_352/library/stdtypes.html#typebytearray).

> 添加于版本2.6。
