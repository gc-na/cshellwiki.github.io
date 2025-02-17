# [Linux] Bash endif 用法: 条件语句的结束标志

## 概述
`endif` 是一个用于 Bash 脚本中的条件语句结束标志。它用于标识 `if` 语句的结束，帮助脚本正确地控制流程。

## 用法
基本语法如下：
```bash
endif
```

## 常用选项
`endif` 命令本身没有选项，因为它只是一个结束标志。它通常与 `if` 语句配合使用。

## 常见示例
以下是一些使用 `endif` 的示例：

### 示例 1: 简单的条件判断
```bash
if [ "$VAR" -eq 1 ]; then
    echo "变量等于 1"
endif
```

### 示例 2: 结合 `else` 使用
```bash
if [ "$VAR" -eq 1 ]; then
    echo "变量等于 1"
else
    echo "变量不等于 1"
endif
```

### 示例 3: 嵌套条件
```bash
if [ "$VAR" -gt 0 ]; then
    echo "变量大于 0"
    if [ "$VAR" -lt 10 ]; then
        echo "变量小于 10"
    endif
endif
```

## 提示
- 确保 `endif` 与 `if` 语句配对使用，以避免语法错误。
- 在复杂的脚本中，保持代码的缩进和格式整齐，可以提高可读性。
- 使用注释来解释条件判断的目的，帮助他人理解代码逻辑。