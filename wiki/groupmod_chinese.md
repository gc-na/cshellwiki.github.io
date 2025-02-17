# [Linux] Bash groupmod 用法: 修改用户组属性

## 概述
`groupmod` 命令用于修改现有用户组的属性。通过此命令，系统管理员可以更改用户组的名称、GID（组标识符）等信息。

## 用法
基本语法如下：
```bash
groupmod [选项] [参数]
```

## 常用选项
- `-n, --new-name <新名称>`: 更改用户组的名称。
- `-g, --gid <新GID>`: 更改用户组的GID。
- `-o, --non-unique`: 允许使用非唯一的GID。

## 常见示例
1. **更改用户组名称**
   ```bash
   groupmod -n newgroup oldgroup
   ```
   这个命令将用户组 `oldgroup` 的名称更改为 `newgroup`。

2. **更改用户组的GID**
   ```bash
   groupmod -g 1001 mygroup
   ```
   该命令将用户组 `mygroup` 的GID更改为 `1001`。

3. **允许非唯一GID**
   ```bash
   groupmod -o -g 1001 anothergroup
   ```
   这个命令将用户组 `anothergroup` 的GID更改为 `1001`，并允许该GID在其他组中重复使用。

## 提示
- 在修改用户组之前，确保没有用户正在使用该组，以避免权限问题。
- 使用 `getent group` 命令可以查看当前系统中的所有用户组及其属性。
- 在更改组名或GID后，检查相关用户的组权限，以确保它们仍然有效。