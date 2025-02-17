# [Linux] Bash w: Xem thông tin người dùng đang đăng nhập

## Overview
Lệnh `w` trong Bash được sử dụng để hiển thị thông tin về người dùng đang đăng nhập vào hệ thống, bao gồm tên người dùng, thời gian đăng nhập, thời gian hoạt động, và các hoạt động hiện tại của họ. Đây là một công cụ hữu ích để theo dõi hoạt động của người dùng trên máy chủ.

## Usage
Cú pháp cơ bản của lệnh `w` như sau:
```
w [options] [arguments]
```

## Common Options
- `-h`: Không hiển thị tiêu đề.
- `-s`: Hiển thị thông tin ngắn gọn.
- `-u`: Hiển thị thời gian hoạt động của người dùng.

## Common Examples
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `w`:

1. **Hiển thị thông tin người dùng đang đăng nhập:**
   ```bash
   w
   ```

2. **Hiển thị thông tin mà không có tiêu đề:**
   ```bash
   w -h
   ```

3. **Hiển thị thông tin ngắn gọn:**
   ```bash
   w -s
   ```

4. **Hiển thị thông tin với thời gian hoạt động của người dùng:**
   ```bash
   w -u
   ```

## Tips
- Sử dụng lệnh `w` để theo dõi hoạt động của người dùng trên máy chủ, đặc biệt là trong môi trường đa người dùng.
- Kết hợp lệnh `w` với các lệnh khác như `grep` để lọc thông tin theo tên người dùng cụ thể.
- Thường xuyên kiểm tra thông tin từ lệnh `w` để phát hiện các hoạt động bất thường trên hệ thống.