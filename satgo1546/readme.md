代码 = 68字节
<br>编译命令的不平庸部分 = 23字节

```sh
cc c.c -DD=`tr %-_ [-~<<<:?t=`
#      ^^^^^^^^^^^^^^^^^^^^^^^
```

用了gcc的多字符字符字面量，\$可作标识符，认定int为4字节，小端序。关键是滥用了内存排布，故为UB，必须在特定编译器和环境下才能正确输出。

即使豁免了main，也躲不过printf等一众函数名。C++有cerr，但#include <iostream>，emm……

感(chāo)谢(le)@MistEO的bash tr解和@nocat的PHP异或解！
