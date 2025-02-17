# [Linux] Bash cksum 用法: 计算文件的校验和

## 概述
`cksum` 命令用于计算文件的校验和（checksum）和字节数。它可以帮助用户验证文件的完整性，确保文件在传输或存储过程中没有被损坏。

## 用法
基本语法如下：
```
cksum [选项] [参数]
```

## 常用选项
- `-a, --algorithm=算法`：指定使用的校验和算法（如 MD5、SHA256 等）。
- `--help`：显示帮助信息。
- `--version`：显示版本信息。

## 常见示例
1. 计算单个文件的校验和：
   ```bash
   cksum filename.txt
   ```

2. 计算多个文件的校验和：
   ```bash
   cksum file1.txt file2.txt
   ```

3. 将输出结果保存到文件中：
   ```bash
   cksum filename.txt > checksum.txt
   ```

4. 使用特定算法计算校验和（假设支持该选项）：
   ```bash
   cksum -a md5 filename.txt
   ```

## 提示
- 在进行文件传输时，建议使用 `cksum` 来验证文件的完整性。
- 将校验和输出重定向到文件中，可以方便后续的比较和验证。
- 对于大文件，计算校验和可能需要一些时间，请耐心等待。