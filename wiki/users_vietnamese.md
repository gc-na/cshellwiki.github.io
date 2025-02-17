# [Linux] Bash users: Quản lý người dùng hệ thống

## Overview
Lệnh `users` trong Bash được sử dụng để hiển thị danh sách các người dùng đang đăng nhập vào hệ thống. Nó cung cấp thông tin nhanh chóng về những ai đang sử dụng máy tính tại thời điểm hiện tại.

## Usage
Cú pháp cơ bản của lệnh `users` như sau:

```bash
users [options]
```

## Common Options
- `-n`: Hiển thị tên người dùng mà không có khoảng trắng.
- `-r`: Hiển thị danh sách người dùng đang đăng nhập theo thứ tự.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `users`:

1. **Hiển thị danh sách người dùng đang đăng nhập:**
   ```bash
   users
   ```

2. **Hiển thị danh sách người dùng mà không có khoảng trắng:**
   ```bash
   users -n
   ```

3. **Hiển thị danh sách người dùng theo thứ tự:**
   ```bash
   users -r
   ```

## Tips
- Sử dụng lệnh `who` để có thêm thông tin chi tiết về người dùng, chẳng hạn như thời gian đăng nhập và địa chỉ IP.
- Kết hợp lệnh `users` với `wc -w` để đếm số lượng người dùng đang đăng nhập:
  ```bash
  users | wc -w
  ```
- Lệnh `users` rất hữu ích trong các kịch bản tự động để theo dõi hoạt động của người dùng trên hệ thống.