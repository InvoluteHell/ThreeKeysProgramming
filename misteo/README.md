# Bash

只能 bash, shell 不行，~~鬼知道为什么 shell 跑不起来~~  

```bash
bash ./misteo.bash
```

然后终端里直接输入会有字符转义问题，所以要多加几个转义符 `\`, 下面这个是可以直接复制粘贴运行的版本

```bash
tr t t<<<$(tr \!-t /-t<<<:)$(tr \!-/ d-t<<<'")),'),\ $(tr /-t +-t<<<[)$(tr \!-/ d-t<<<',/)')d!
```

## 简单解释

[tr 命令](https://www.runoob.com/linux/linux-comm-tr.html)

`tr \!-t /-t<<<:` 这个把 `:` 转换成 `H`， `tr ,-t --t<<<d` 把 `d` 转换成 `e`，后面都是同理
