# [Linux] Bash popd 用法: 从目录栈中移除目录

## 概述
`popd` 命令用于从目录栈中移除顶部的目录，并切换到新的顶部目录。它是与 `pushd` 命令配合使用的，后者用于将当前目录推入目录栈。

## 用法
基本语法如下：
```
popd [options]
```

## 常用选项
- `-n`：不改变当前目录，仅从目录栈中移除目录。
- `+N`：移除目录栈中第 N 个目录，而不是顶部的目录。
- `-N`：移除目录栈中倒数第 N 个目录，并切换到新的顶部目录。

## 常见示例
1. **基本用法**：从目录栈中移除顶部目录并切换到下一个目录。
   ```bash
   pushd /path/to/dir1
   pushd /path/to/dir2
   popd
   ```

2. **使用 `-n` 选项**：仅移除目录而不切换。
   ```bash
   pushd /path/to/dir1
   pushd /path/to/dir2
   popd -n
   ```

3. **使用 `+N` 选项**：移除目录栈中指定的目录。
   ```bash
   pushd /path/to/dir1
   pushd /path/to/dir2
   pushd /path/to/dir3
   popd +1
   ```

4. **使用 `-N` 选项**：移除倒数第 N 个目录并切换。
   ```bash
   pushd /path/to/dir1
   pushd /path/to/dir2
   pushd /path/to/dir3
   popd -2
   ```

## 提示
- 在使用 `popd` 之前，确保你已经使用 `pushd` 添加了目录到栈中。
- 使用 `dirs` 命令可以查看当前的目录栈状态。
- 结合 `pushd` 和 `popd` 可以方便地在多个目录之间切换，提升工作效率。