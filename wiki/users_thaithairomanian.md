# [Linux] Bash users sử dụng: Quản lý người dùng hệ thống

## Overview
Lệnh `users` trong Bash được sử dụng để hiển thị danh sách tên người dùng đang đăng nhập vào hệ thống. Đây là một công cụ hữu ích để theo dõi ai đang sử dụng máy chủ hoặc máy tính của bạn tại một thời điểm cụ thể.

## Usage
Cú pháp cơ bản của lệnh `users` như sau:
```bash
users [options]
```

## Common Options
- `-n`: Hiển thị số lượng người dùng đang đăng nhập.
- `-r`: Chỉ hiển thị tên người dùng đang đăng nhập từ một terminal cụ thể.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `users`:

1. Hiển thị danh sách tất cả người dùng đang đăng nhập:
   ```bash
   users
   ```

2. Hiển thị số lượng người dùng đang đăng nhập:
   ```bash
   users -n
   ```

3. Hiển thị người dùng từ một terminal cụ thể (ví dụ: tty1):
   ```bash
   users -r tty1
   ```

## Tips
- Sử dụng lệnh `who` để có thêm thông tin chi tiết về người dùng, bao gồm thời gian đăng nhập và địa chỉ IP.
- Kết hợp lệnh `users` với các lệnh khác như `wc -l` để đếm số lượng người dùng đang đăng nhập:
  ```bash
  users | wc -w
  ```
- Thường xuyên kiểm tra người dùng đang đăng nhập để đảm bảo an ninh cho hệ thống của bạn.