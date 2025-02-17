# [Linux] Bash printf 用法: 格式化输出文本

## 概述
`printf` 命令用于格式化输出文本。它允许用户按照指定的格式打印字符串、数字和其他数据类型，提供比 `echo` 更加灵活的输出选项。

## 用法
基本语法如下：
```bash
printf [options] [arguments]
```

## 常用选项
- `-v var`: 将输出存储到变量 `var` 中，而不是打印到标准输出。
- `-f format`: 指定输出的格式。
- `--help`: 显示帮助信息。
- `--version`: 显示版本信息。

## 常见示例
1. **基本字符串输出**
   ```bash
   printf "Hello, World!\n"
   ```

2. **格式化数字输出**
   ```bash
   printf "Number: %d\n" 42
   ```

3. **输出浮点数**
   ```bash
   printf "Float: %.2f\n" 3.14159
   ```

4. **输出多个变量**
   ```bash
   name="Alice"
   age=30
   printf "%s is %d years old.\n" "$name" "$age"
   ```

5. **使用变量存储输出**
   ```bash
   output=$(printf "Hello, %s!\n" "Bob")
   echo "$output"
   ```

## 提示
- 使用格式说明符（如 `%s`, `%d`, `%f`）可以确保输出的格式符合预期。
- 注意换行符 `\n` 的使用，以确保输出的整洁。
- 可以使用 `-v` 选项将格式化的输出存储到变量中，便于后续使用。