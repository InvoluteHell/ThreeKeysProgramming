# Bash

```bash
bash ./misteo.bash
```

只能 bash, shell 不行，~~鬼知道这玩意怎么跑起来的~~  

终端里直接输入会有字符转义问题，所以要多加几个转义符 `\`, 下面这个是可以直接复制粘贴运行的版本

```bash
tr -d \\`tr %-t \!-t<<<r` <<<`tr \!-t /-t<<<:;tr ,-t --t<<<d;tr %-t --t<<<d;tr %-t --t<<<d;tr /-t ,-t<<<r;`", "`tr /-t +-t<<<[;tr /-t ,-t<<<r;`"r"`tr %-t --t<<<d`"d\!"
```
