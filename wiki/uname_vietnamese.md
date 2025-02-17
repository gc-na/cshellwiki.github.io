# [Linux] Bash uname cách sử dụng: Hiển thị thông tin hệ thống

## Tổng quan
Lệnh `uname` trong Bash được sử dụng để hiển thị thông tin về hệ thống đang chạy, bao gồm tên kernel, tên máy, phiên bản kernel và nhiều thông tin khác. Đây là một công cụ hữu ích để kiểm tra cấu hình hệ thống của bạn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `uname` như sau:

```bash
uname [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`: Hiển thị tất cả thông tin hệ thống.
- `-s`: Hiển thị tên kernel.
- `-n`: Hiển thị tên máy.
- `-r`: Hiển thị phiên bản kernel.
- `-v`: Hiển thị thông tin phiên bản.
- `-m`: Hiển thị kiến trúc máy.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `uname`:

1. Hiển thị tất cả thông tin hệ thống:
   ```bash
   uname -a
   ```

2. Hiển thị tên kernel:
   ```bash
   uname -s
   ```

3. Hiển thị tên máy:
   ```bash
   uname -n
   ```

4. Hiển thị phiên bản kernel:
   ```bash
   uname -r
   ```

5. Hiển thị kiến trúc máy:
   ```bash
   uname -m
   ```

## Mẹo
- Sử dụng `uname -a` để có cái nhìn tổng quát về hệ thống của bạn trong một lệnh duy nhất.
- Kết hợp lệnh `uname` với các lệnh khác trong Bash để tự động hóa việc kiểm tra thông tin hệ thống trong các script.
- Thường xuyên kiểm tra phiên bản kernel để đảm bảo rằng bạn đang sử dụng phiên bản mới nhất và an toàn.