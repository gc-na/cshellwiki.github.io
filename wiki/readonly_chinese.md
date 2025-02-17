# [Linux] Bash readonly 用法: 设置只读变量

## 概述
`readonly` 命令用于将变量标记为只读，防止其在后续的脚本或命令中被修改。这对于保护重要的配置值或常量非常有用。

## 用法
基本语法如下：
```bash
readonly [options] [arguments]
```

## 常用选项
- `-p`：显示所有只读变量及其值。

## 常见示例
1. **设置只读变量**
   ```bash
   readonly MY_VAR="Hello, World!"
   ```

2. **尝试修改只读变量**
   ```bash
   MY_VAR="New Value"  # 这将会报错
   ```

3. **查看只读变量**
   ```bash
   readonly -p  # 显示所有只读变量
   ```

4. **在脚本中使用只读变量**
   ```bash
   #!/bin/bash
   readonly CONFIG_PATH="/etc/myconfig"
   echo "配置文件路径是: $CONFIG_PATH"
   ```

## 提示
- 在定义重要的常量时使用 `readonly`，可以避免意外修改。
- 使用 `readonly -p` 可以快速检查当前所有只读变量，方便调试。
- 只读变量的作用域与普通变量相同，可以在函数内部使用，但不能在函数内修改。