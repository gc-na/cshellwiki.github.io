# [Linux] Bash tmux cách sử dụng: Quản lý phiên làm việc trong terminal

## Overview
Tmux là một trình quản lý phiên làm việc trong terminal, cho phép người dùng tạo, quản lý và điều khiển nhiều phiên làm việc trong một cửa sổ terminal duy nhất. Điều này rất hữu ích cho việc tổ chức công việc và làm việc với nhiều tác vụ cùng một lúc.

## Usage
Cú pháp cơ bản của lệnh tmux như sau:
```
tmux [options] [arguments]
```

## Common Options
- `new`: Tạo một phiên tmux mới.
- `attach`: Kết nối lại với một phiên tmux đã tồn tại.
- `detach`: Ngắt kết nối khỏi phiên tmux hiện tại.
- `list-sessions`: Liệt kê tất cả các phiên tmux đang chạy.
- `kill-session`: Kết thúc một phiên tmux cụ thể.

## Common Examples
- Tạo một phiên tmux mới:
  ```bash
  tmux new -s mysession
  ```
- Kết nối lại với một phiên tmux đã tồn tại:
  ```bash
  tmux attach -t mysession
  ```
- Ngắt kết nối khỏi phiên tmux hiện tại:
  ```bash
  Ctrl + b, d
  ```
- Liệt kê tất cả các phiên tmux:
  ```bash
  tmux list-sessions
  ```
- Kết thúc một phiên tmux cụ thể:
  ```bash
  tmux kill-session -t mysession
  ```

## Tips
- Sử dụng tổ hợp phím `Ctrl + b` để truy cập các lệnh tmux nhanh chóng.
- Đặt tên cho các phiên tmux để dễ dàng quản lý và phân biệt.
- Sử dụng tmux trong các tác vụ dài để có thể ngắt kết nối và quay lại mà không mất tiến trình làm việc.