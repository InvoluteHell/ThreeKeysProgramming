# 为什么这工作？

众所周知， Python 可以用 `exec` 把字符串当作字母使用，而这刚好只有三种字母。而另一方面，通过 `'%c'` 字符串（复用了 `exec` 中的 `c`）和格式化操作符 `%` 我们可以把数字变成字符。最后，用 `()=()` 造出 `True`, 再通过 `-~` 之类的方法把它变成数字，剩下的工作就只是凑数字。

凑数字的方式大概还能再优化，留作习题。

灵感来源：https://codegolf.stackexchange.com/questions/178970/no-alphanumeric-code-exec