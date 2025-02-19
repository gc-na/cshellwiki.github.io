# [Hệ điều hành] C Shell (csh) tmux: Quản lý phiên làm việc trong terminal

## Tổng quan
Tmux là một trình quản lý phiên làm việc trong terminal, cho phép người dùng tạo, quản lý và chia sẻ các phiên làm việc. Với tmux, bạn có thể chạy nhiều phiên làm việc trong cùng một cửa sổ terminal, giúp tăng hiệu suất làm việc và quản lý các tác vụ dễ dàng hơn.

## Cú pháp
Cú pháp cơ bản của lệnh tmux như sau:
```bash
tmux [options] [arguments]
```

## Các tùy chọn phổ biến
- `new`: Tạo một phiên tmux mới.
- `attach`: Kết nối lại với một phiên tmux đã tồn tại.
- `detach`: Ngắt kết nối khỏi phiên tmux hiện tại.
- `list-sessions`: Liệt kê tất cả các phiên tmux đang hoạt động.
- `kill-session`: Kết thúc một phiên tmux cụ thể.

## Ví dụ phổ biến
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

## Mẹo
- Sử dụng phím tắt `Ctrl + b` để truy cập vào các lệnh tmux nhanh chóng.
- Đặt tên cho các phiên tmux để dễ dàng quản lý và phân biệt.
- Sử dụng tmux trong các tác vụ dài để có thể ngắt kết nối và quay lại mà không mất tiến trình làm việc.