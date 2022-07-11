## 六键成码

### 使用字符串

`G`

`1`

`char` ❌

### 运行环境

LuaJIT 2.1，该方案依赖 Lua 5.1 标准中整浮点数隐式向整数转换的特性

### 运行结果

```
$ luajit -v
LuaJIT 2.1.0-beta3 -- Copyright (C) 2005-2022 Mike Pall. https://luajit.org/
$ luajit G1.lua 
Hello, World!
$ _
```

### 实现方法与失败原因

Lua 中所有字符串类型值的 `__index` 元方法都指向 `string`，故可用 `("").char` 形式获取到 `string.char` 函数，用以转换 ASCII 码

Lua 中 `string.char(...)` 能够接受字符串形式的整数，故连接操作符（`..`）产生的字符串可在此使用

Lua（5.1）中全局变量存在于一张名为 `_G` 的表之中，故可直接索引该表得到 `print` 函数

Lua（在夏末的认知）中存在且仅存在 `string.char(...)` 可用于转化 ASCII 码（形如 `\111` 的字面量等方法在此处无法使用），故该方案失败

----

### omo
