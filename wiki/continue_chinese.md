# [Linux] Bash continue 用法: 继续循环的命令

## 概述
`continue` 命令用于在循环中跳过当前迭代的剩余部分，并开始下一次迭代。它通常与 `for`、`while` 或 `until` 循环一起使用。

## 用法
基本语法如下：
```
continue [n]
```
其中 `n` 是可选参数，表示跳过的循环层级。

## 常用选项
- `n`：指定要跳过的循环层级，默认为 1，表示跳过当前循环。

## 常见示例
以下是一些使用 `continue` 命令的实际示例：

### 示例 1: 跳过偶数
```bash
for i in {1..10}; do
    if (( i % 2 == 0 )); then
        continue
    fi
    echo $i
done
```
这个示例将打印 1 到 10 之间的所有奇数。

### 示例 2: 跳过特定值
```bash
for i in {1..10}; do
    if [ $i -eq 5 ]; then
        continue
    fi
    echo $i
done
```
在这个示例中，数字 5 将被跳过，输出将是 1 到 10 之间的所有数字，除了 5。

### 示例 3: 在 while 循环中使用
```bash
count=1
while [ $count -le 10 ]; do
    if [ $count -eq 3 ]; then
        count=$((count + 1))
        continue
    fi
    echo $count
    count=$((count + 1))
done
```
这个示例在 `while` 循环中跳过了数字 3。

## 小贴士
- 使用 `continue` 时，确保你了解循环的结构，以避免意外跳过重要的代码。
- 在多层嵌套循环中使用 `n` 参数时，注意它会影响到外层循环的行为。
- 适当使用 `continue` 可以使代码更简洁，提高可读性。