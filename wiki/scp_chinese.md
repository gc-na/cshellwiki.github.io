# [Linux] Bash scp 用法: 远程文件传输

## 概述
`scp`（Secure Copy Protocol）命令用于在本地和远程主机之间安全地复制文件。它基于SSH协议，确保数据在传输过程中的安全性。

## 用法
基本语法如下：
```bash
scp [选项] [源文件] [目标]
```

## 常用选项
- `-r`：递归复制整个目录。
- `-P`：指定远程主机的端口号（注意是大写的P）。
- `-i`：指定用于身份验证的私钥文件。
- `-v`：详细模式，显示传输过程中的详细信息。
- `-q`：安静模式，不显示任何进度信息。

## 常见示例
1. 从本地复制文件到远程主机：
   ```bash
   scp /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

2. 从远程主机复制文件到本地：
   ```bash
   scp username@remote_host:/path/to/remote/file /path/to/local/directory
   ```

3. 递归复制整个目录到远程主机：
   ```bash
   scp -r /path/to/local/directory username@remote_host:/path/to/remote/directory
   ```

4. 使用指定端口号进行复制：
   ```bash
   scp -P 2222 /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

5. 使用私钥文件进行身份验证：
   ```bash
   scp -i /path/to/private_key /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

## 小贴士
- 在使用`scp`时，确保目标路径的权限设置正确，以避免权限不足的问题。
- 使用`-v`选项可以帮助你调试连接问题。
- 如果需要频繁传输文件，可以考虑使用`rsync`，它提供了更多的功能和灵活性。