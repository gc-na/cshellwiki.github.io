# [Linux] Bash ssh cách sử dụng: Kết nối an toàn đến máy chủ từ xa

## Overview
Lệnh `ssh` (Secure Shell) được sử dụng để kết nối an toàn đến một máy chủ từ xa. Nó cho phép người dùng thực hiện các lệnh trên máy chủ từ xa và quản lý các hệ thống một cách an toàn thông qua mạng.

## Usage
Cú pháp cơ bản của lệnh `ssh` như sau:

```bash
ssh [options] [user@]hostname
```

## Common Options
- `-p PORT`: Chỉ định cổng kết nối (mặc định là 22).
- `-i FILE`: Sử dụng khóa riêng từ tệp FILE để xác thực.
- `-v`: Bật chế độ chi tiết để xem thông tin kết nối.
- `-X`: Cho phép chuyển tiếp giao diện đồ họa X11.
- `-C`: Kích hoạt nén dữ liệu để tăng tốc độ truyền tải.

## Common Examples
- Kết nối đến máy chủ với tên người dùng mặc định:

```bash
ssh username@hostname
```

- Kết nối đến máy chủ trên cổng khác:

```bash
ssh -p 2222 username@hostname
```

- Kết nối với khóa riêng:

```bash
ssh -i ~/.ssh/id_rsa username@hostname
```

- Kết nối và bật chế độ chi tiết:

```bash
ssh -v username@hostname
```

- Kết nối với chuyển tiếp X11:

```bash
ssh -X username@hostname
```

## Tips
- Luôn sử dụng khóa SSH thay vì mật khẩu để tăng cường bảo mật.
- Kiểm tra kết nối trước khi thực hiện các lệnh quan trọng để tránh mất dữ liệu.
- Sử dụng tệp cấu hình `~/.ssh/config` để lưu trữ các tùy chọn kết nối thường dùng, giúp tiết kiệm thời gian khi kết nối.