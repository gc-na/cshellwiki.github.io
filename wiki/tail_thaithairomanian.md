# [Linux] Bash tail sử dụng: Hiển thị nội dung cuối của tệp

## Overview
Lệnh `tail` trong Bash được sử dụng để hiển thị các dòng cuối cùng của một tệp. Đây là công cụ hữu ích để theo dõi các tệp log hoặc xem nội dung mới được thêm vào mà không cần mở toàn bộ tệp.

## Usage
Cú pháp cơ bản của lệnh `tail` như sau:
```bash
tail [options] [arguments]
```

## Common Options
- `-n [number]`: Hiển thị số dòng cuối cùng cụ thể từ tệp.
- `-f`: Theo dõi tệp theo thời gian thực, hiển thị các dòng mới được thêm vào.
- `-c [number]`: Hiển thị số byte cuối cùng cụ thể từ tệp.

## Common Examples
- Hiển thị 10 dòng cuối cùng của tệp `example.txt`:
  ```bash
  tail example.txt
  ```

- Hiển thị 20 dòng cuối cùng của tệp `logfile.log`:
  ```bash
  tail -n 20 logfile.log
  ```

- Theo dõi tệp `access.log` để xem các dòng mới được thêm vào:
  ```bash
  tail -f access.log
  ```

- Hiển thị 50 byte cuối cùng của tệp `data.txt`:
  ```bash
  tail -c 50 data.txt
  ```

## Tips
- Sử dụng `tail -f` để theo dõi các tệp log trong thời gian thực, điều này rất hữu ích cho việc gỡ lỗi.
- Kết hợp `tail` với các lệnh khác như `grep` để lọc thông tin cụ thể từ tệp.
- Bạn có thể sử dụng `tail` trong các script để tự động xử lý các tệp log hoặc dữ liệu mới.