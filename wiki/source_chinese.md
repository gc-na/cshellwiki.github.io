# [Linux] Bash source 用法：执行脚本文件

## 概述
`source` 命令用于在当前 shell 环境中执行指定的脚本文件。与直接运行脚本不同，使用 `source` 可以使得脚本中的变量和函数在当前 shell 中可用，而不是在子 shell 中执行。

## 用法
基本语法如下：
```
source [选项] [参数]
```

## 常用选项
- `-`：不常用，通常可以忽略。
  
## 常见示例

### 示例 1：执行脚本文件
假设有一个名为 `script.sh` 的脚本文件，内容如下：
```bash
#!/bin/bash
export MY_VAR="Hello, World!"
```
可以使用 `source` 命令来执行这个脚本：
```bash
source script.sh
```
执行后，`MY_VAR` 变量将在当前 shell 中可用。

### 示例 2：使用点号代替 source
`source` 命令可以用点号 `.` 来代替，效果相同：
```bash
. script.sh
```

### 示例 3：在脚本中定义函数
如果 `script.sh` 中定义了一个函数，可以在当前 shell 中直接调用：
```bash
#!/bin/bash
my_function() {
    echo "This is my function!"
}
```
执行后：
```bash
source script.sh
my_function
```
输出将是：
```
This is my function!
```

## 提示
- 使用 `source` 来加载环境变量或函数时，确保脚本的路径正确。
- 通过 `source` 加载的变量和函数在当前 shell 会话中保持有效，直到会话结束或变量被重置。
- 如果脚本中有错误，`source` 会在当前 shell 中停止执行，便于调试。