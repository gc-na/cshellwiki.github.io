# [Linux] Bash ps sử dụng: Hiển thị thông tin về tiến trình

## Overview
Lệnh `ps` được sử dụng để hiển thị thông tin về các tiến trình đang chạy trên hệ thống. Nó giúp người dùng theo dõi và quản lý các tiến trình, cho phép xem các thông tin như ID tiến trình, trạng thái, và tài nguyên mà tiến trình đang sử dụng.

## Usage
Cú pháp cơ bản của lệnh `ps` như sau:
```
ps [options] [arguments]
```

## Common Options
- `-e` hoặc `-A`: Hiển thị tất cả các tiến trình.
- `-f`: Hiển thị thông tin chi tiết về tiến trình.
- `-u [user]`: Hiển thị các tiến trình của một người dùng cụ thể.
- `-aux`: Hiển thị tất cả các tiến trình với thông tin chi tiết.
- `--sort`: Sắp xếp kết quả theo một tiêu chí nhất định.

## Common Examples
- Hiển thị tất cả các tiến trình đang chạy:
  ```bash
  ps -e
  ```

- Hiển thị thông tin chi tiết về tất cả các tiến trình:
  ```bash
  ps -ef
  ```

- Hiển thị các tiến trình của một người dùng cụ thể:
  ```bash
  ps -u username
  ```

- Hiển thị tất cả các tiến trình với thông tin chi tiết:
  ```bash
  ps aux
  ```

- Sắp xếp các tiến trình theo mức sử dụng CPU:
  ```bash
  ps aux --sort=-%cpu
  ```

## Tips
- Sử dụng `ps aux` để có cái nhìn tổng quan về tất cả các tiến trình và tài nguyên mà chúng đang sử dụng.
- Kết hợp với lệnh `grep` để tìm kiếm một tiến trình cụ thể:
  ```bash
  ps aux | grep process_name
  ```
- Thường xuyên kiểm tra tiến trình để phát hiện và xử lý các vấn đề tiềm ẩn trên hệ thống.