# [Linux] Bash lvextend 用法: 扩展逻辑卷的大小

## 概述
`lvextend` 命令用于扩展逻辑卷（Logical Volume, LV）的大小。通过增加逻辑卷的大小，用户可以为文件系统提供更多的存储空间。

## 用法
基本语法如下：
```bash
lvextend [options] [arguments]
```

## 常用选项
- `-L +size`：增加逻辑卷的大小，例如 `-L +10G` 表示增加 10GB。
- `-l +size`：按逻辑扩展单元（LE）增加大小，例如 `-l +100` 表示增加 100 个逻辑扩展单元。
- `-r`：在扩展逻辑卷的同时自动扩展文件系统。
- `-n`：指定新的逻辑卷名称。

## 常见示例
1. 增加逻辑卷的大小 10GB：
   ```bash
   lvextend -L +10G /dev/vgname/lvname
   ```

2. 按逻辑扩展单元增加 100 个 LE：
   ```bash
   lvextend -l +100 /dev/vgname/lvname
   ```

3. 扩展逻辑卷并自动扩展文件系统：
   ```bash
   lvextend -r -L +5G /dev/vgname/lvname
   ```

4. 更改逻辑卷名称：
   ```bash
   lvextend -n newlvname /dev/vgname/lvname
   ```

## 提示
- 在扩展逻辑卷之前，确保有足够的物理空间可用。
- 使用 `-r` 选项可以简化操作，避免手动扩展文件系统。
- 在生产环境中操作前，建议备份重要数据，以防意外情况发生。