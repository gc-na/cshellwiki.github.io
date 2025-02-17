# [Linux] Bash tmux Sử dụng: Quản lý phiên làm việc trong terminal

## Overview
tmux là một trình quản lý phiên làm việc trong terminal, cho phép người dùng tạo, quản lý và chuyển đổi giữa nhiều phiên làm việc trong cùng một cửa sổ terminal. Điều này rất hữu ích cho việc tổ chức công việc và duy trì các phiên làm việc lâu dài.

## Usage
Cú pháp cơ bản của lệnh tmux như sau:
```bash
tmux [options] [arguments]
```

## Common Options
- `new`: Tạo một phiên tmux mới.
- `attach`: Kết nối lại với một phiên tmux đã tồn tại.
- `detach`: Ngắt kết nối khỏi phiên tmux hiện tại.
- `list-sessions`: Liệt kê tất cả các phiên tmux đang hoạt động.
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
- Kết thúc một phiên tmux:
  ```bash
  tmux kill-session -t mysession
  ```

## Tips
- Sử dụng tổ hợp phím `Ctrl + b` để kích hoạt các lệnh tmux.
- Đặt tên cho các phiên tmux của bạn để dễ dàng quản lý và nhận diện.
- Sử dụng tmux trong các tác vụ dài hạn để duy trì tiến trình ngay cả khi bạn ngắt kết nối khỏi terminal.