# [Linux] Bash wget 用法：下载文件的命令行工具

## 概述
`wget` 是一个用于从网络上下载文件的命令行工具。它支持 HTTP、HTTPS 和 FTP 协议，可以在不需要用户交互的情况下下载文件，非常适合批量下载和自动化任务。

## 用法
基本语法如下：
```bash
wget [选项] [参数]
```

## 常用选项
- `-O <文件名>`：指定下载文件的名称。
- `-c`：继续未完成的下载。
- `-q`：安静模式，不显示下载进度。
- `--limit-rate=<速率>`：限制下载速度。
- `-r`：递归下载，适用于下载整个网站。

## 常见示例
1. 下载单个文件：
   ```bash
   wget https://example.com/file.zip
   ```

2. 指定下载文件名：
   ```bash
   wget -O myfile.zip https://example.com/file.zip
   ```

3. 继续未完成的下载：
   ```bash
   wget -c https://example.com/file.zip
   ```

4. 安静模式下载：
   ```bash
   wget -q https://example.com/file.zip
   ```

5. 限制下载速度：
   ```bash
   wget --limit-rate=200k https://example.com/file.zip
   ```

6. 递归下载整个网站：
   ```bash
   wget -r https://example.com/
   ```

## 小贴士
- 使用 `-c` 选项可以避免重复下载大文件，节省时间和带宽。
- 在下载大量文件时，考虑使用 `-r` 选项，并结合 `--no-parent` 选项，以避免下载父目录中的文件。
- 定期检查 wget 的版本更新，以获取最新的功能和修复。