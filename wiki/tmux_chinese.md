# [Linux] Bash tmux 使用: 终端复用工具

## 概述
tmux 是一个终端复用器，它允许用户在一个单一的窗口中创建和管理多个终端会话。通过 tmux，用户可以在一个屏幕上同时运行多个命令行程序，并在它们之间轻松切换。

## 用法
tmux 的基本语法如下：

```bash
tmux [options] [arguments]
```

## 常用选项
- `new`: 创建一个新的 tmux 会话。
- `attach`: 附加到一个已经存在的 tmux 会话。
- `list-sessions`: 列出所有当前的 tmux 会话。
- `kill-session`: 终止一个指定的 tmux 会话。
- `detach`: 从当前会话中分离。

## 常见示例
1. 创建一个新的 tmux 会话：
   ```bash
   tmux new -s mysession
   ```

2. 附加到一个已经存在的会话：
   ```bash
   tmux attach -t mysession
   ```

3. 列出所有当前的会话：
   ```bash
   tmux list-sessions
   ```

4. 终止一个指定的会话：
   ```bash
   tmux kill-session -t mysession
   ```

5. 从当前会话中分离：
   ```bash
   Ctrl+b 然后按 d
   ```

## 小贴士
- 使用 `tmux` 的命令行快捷键（如 `Ctrl+b`）可以提高工作效率。
- 可以通过配置文件（如 `~/.tmux.conf`）自定义 tmux 的行为和外观。
- 定期保存会话，以便在需要时快速恢复工作环境。