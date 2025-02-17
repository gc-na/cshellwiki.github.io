# [Linux] Bash usermod 使用方法: 修改用户账户信息

## 概述
`usermod` 命令用于修改现有用户的账户信息，包括用户的组、主目录、登录名等。它是系统管理员管理用户账户的重要工具。

## 用法
基本语法如下：
```bash
usermod [选项] [参数]
```

## 常用选项
- `-aG`：将用户添加到附加组中，而不移除其原有组。
- `-d`：指定用户的新主目录。
- `-l`：更改用户的登录名。
- `-s`：更改用户的登录 shell。
- `-g`：指定用户的新主组。

## 常见示例
1. 将用户 `john` 添加到 `sudo` 组：
   ```bash
   usermod -aG sudo john
   ```

2. 更改用户 `mary` 的主目录为 `/home/mary_new`：
   ```bash
   usermod -d /home/mary_new mary
   ```

3. 更改用户 `alice` 的登录名为 `alice_new`：
   ```bash
   usermod -l alice_new alice
   ```

4. 更改用户 `bob` 的默认 shell 为 `/bin/bash`：
   ```bash
   usermod -s /bin/bash bob
   ```

5. 将用户 `charlie` 的主组更改为 `developers`：
   ```bash
   usermod -g developers charlie
   ```

## 小贴士
- 在使用 `usermod` 命令之前，建议备份用户的原始信息，以防出现错误。
- 确保在修改用户信息后，用户重新登录以使更改生效。
- 使用 `-aG` 选项时，要特别注意，确保在添加用户到新组时不移除其原有组。