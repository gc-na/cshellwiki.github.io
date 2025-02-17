# [Linux] Bash umask 用法: 设置默认文件权限

## 概述
`umask` 命令用于设置新创建文件和目录的默认权限掩码。它决定了在创建文件或目录时，哪些权限将被禁用。

## 用法
基本语法如下：
```bash
umask [options] [arguments]
```

## 常用选项
- `-S`：以符号方式显示当前的 umask 值。
- `-p`：以可读的格式显示当前的 umask 值。

## 常见示例
1. 查看当前 umask 值：
   ```bash
   umask
   ```

2. 设置 umask 值为 022（新文件权限为 644，目录权限为 755）：
   ```bash
   umask 022
   ```

3. 使用符号方式查看 umask 值：
   ```bash
   umask -S
   ```

4. 设置 umask 值为 007（新文件权限为 660，目录权限为 770）：
   ```bash
   umask 007
   ```

## 提示
- 在设置 umask 值时，确保了解其对文件和目录权限的影响，以避免不必要的权限问题。
- 可以在用户的 shell 配置文件（如 `.bashrc` 或 `.bash_profile`）中设置 umask 值，以便每次登录时自动应用。
- 使用 `umask -S` 可以更直观地理解当前的权限设置。