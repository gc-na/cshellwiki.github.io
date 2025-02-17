# [Linux] Bash mkfifo 用法: 创建命名管道

## 概述
`mkfifo` 命令用于创建命名管道（FIFO），这是一种特殊类型的文件，允许进程之间进行通信。命名管道可以在不同的进程之间传递数据，通常用于实现生产者-消费者模型。

## 用法
基本语法如下：
```
mkfifo [选项] [参数]
```

## 常用选项
- `-m, --mode=MODE`：设置新建管道的权限模式，默认为 0666。
- `--help`：显示帮助信息。
- `--version`：显示版本信息。

## 常见示例
1. 创建一个简单的命名管道：
   ```bash
   mkfifo mypipe
   ```

2. 创建一个具有特定权限的命名管道：
   ```bash
   mkfifo -m 0644 mypipe
   ```

3. 在一个终端中读取命名管道的数据：
   ```bash
   cat mypipe
   ```

4. 在另一个终端中向命名管道写入数据：
   ```bash
   echo "Hello, World!" > mypipe
   ```

5. 使用命名管道进行进程间通信：
   ```bash
   mkfifo mypipe
   (echo "Data from producer" > mypipe) &
   (cat mypipe) &
   ```

## 提示
- 在使用 `mkfifo` 创建命名管道后，确保有相应的进程在读取或写入数据，否则命令可能会阻塞。
- 使用 `ls -l` 命令可以查看命名管道的权限和状态。
- 命名管道的删除与普通文件相同，可以使用 `rm` 命令删除。