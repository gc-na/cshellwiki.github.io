# [Linux] Bash break 用法: 退出循环

## 概述
`break` 命令用于在 Bash 脚本或命令行中退出循环结构。它可以用于 `for`、`while` 和 `until` 循环，帮助程序在满足特定条件时提前终止循环。

## 用法
基本语法如下：
```bash
break [n]
```
其中 `n` 是一个可选参数，表示要退出的循环层级，默认值为 1。

## 常见选项
- `n`：指定要退出的循环层级。如果有嵌套循环，可以使用此参数退出特定层级的循环。

## 常见示例
以下是一些常见的 `break` 使用示例：

### 示例 1: 基本用法
退出一个简单的 `for` 循环：
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo $i
done
```
输出：
```
1
2
```

### 示例 2: 退出嵌套循环
退出外层循环：
```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $i -eq 2 ]; then
      break 2
    fi
    echo "i: $i, j: $j"
  done
done
```
输出：
```
i: 1, j: 1
i: 1, j: 2
i: 1, j: 3
```

### 示例 3: 使用条件退出
根据用户输入退出循环：
```bash
while true; do
  read -p "输入 'exit' 退出循环: " input
  if [ "$input" == "exit" ]; then
    break
  fi
  echo "你输入了: $input"
done
```

## 提示
- 在使用 `break` 时，确保逻辑清晰，以避免意外退出循环。
- 使用 `break n` 可以有效管理嵌套循环，避免复杂的条件判断。
- 在调试脚本时，可以使用 `echo` 语句跟踪循环的执行情况，帮助理解 `break` 的效果。