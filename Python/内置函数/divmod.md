# [内置函数](https://github.com/Summer-Felix/Develop/blob/master/Python/内置函数.md) #

## [divmod()](http://python.usyiyi.cn/translate/python_352/library/functions.html) ##

divmod(a, b)

取两个（非复数）数字作为参数，并在使用整数除法时返回由商和余数组成的一对数字。

对于混合的操作数类型，应用二元算术运算符的规则。

对于整数，结果与（a // b， a ％ b）相同。

对于浮点数，结果为（q， a ％ b），其中q通常为math.floor(a / b)，也有可能比这个结果小1。

不管怎样，q * b + a % b非常接近于a，如果a % b非0，它和b符号相同且0 <= abs(a % b) < abs(b)。
