# [Linux] Bash ps Cách sử dụng: Hiển thị thông tin tiến trình

## Overview
Lệnh `ps` trong Bash được sử dụng để hiển thị thông tin về các tiến trình đang chạy trên hệ thống. Nó cung cấp cái nhìn tổng quan về các tiến trình, bao gồm ID tiến trình, trạng thái và tài nguyên mà chúng đang sử dụng.

## Usage
Cú pháp cơ bản của lệnh `ps` như sau:
```
ps [options] [arguments]
```

## Common Options
- `-e`: Hiển thị tất cả các tiến trình đang chạy.
- `-f`: Hiển thị thông tin chi tiết về tiến trình, bao gồm cả PID cha.
- `-u [user]`: Hiển thị tiến trình của một người dùng cụ thể.
- `-aux`: Hiển thị tất cả các tiến trình với thông tin chi tiết.
- `--sort [key]`: Sắp xếp kết quả theo khóa chỉ định (ví dụ: `pid`, `user`, `time`).

## Common Examples
- Hiển thị tất cả các tiến trình đang chạy:
  ```bash
  ps -e
  ```
  
- Hiển thị thông tin chi tiết về các tiến trình:
  ```bash
  ps -f
  ```

- Hiển thị tiến trình của một người dùng cụ thể:
  ```bash
  ps -u username
  ```

- Hiển thị tất cả các tiến trình với thông tin chi tiết:
  ```bash
  ps aux
  ```

- Sắp xếp các tiến trình theo thời gian sử dụng CPU:
  ```bash
  ps aux --sort=-%cpu
  ```

## Tips
- Sử dụng `ps aux` để có cái nhìn tổng quan nhất về tất cả các tiến trình.
- Kết hợp `ps` với `grep` để tìm kiếm một tiến trình cụ thể:
  ```bash
  ps aux | grep process_name
  ```
- Thường xuyên kiểm tra tiến trình để theo dõi hiệu suất hệ thống và phát hiện các vấn đề tiềm ẩn.