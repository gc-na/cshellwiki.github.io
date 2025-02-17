# [Linux] Bash dpkg Sử dụng: Quản lý gói phần mềm

## Overview
Lệnh `dpkg` là công cụ quản lý gói cho hệ điều hành Debian và các bản phân phối dựa trên Debian, như Ubuntu. Nó cho phép người dùng cài đặt, gỡ bỏ và quản lý các gói phần mềm trên hệ thống.

## Usage
Cú pháp cơ bản của lệnh `dpkg` như sau:
```
dpkg [options] [arguments]
```

## Common Options
- `-i`, `--install`: Cài đặt gói từ file `.deb`.
- `-r`, `--remove`: Gỡ bỏ gói đã cài đặt.
- `-l`, `--list`: Liệt kê tất cả các gói đã cài đặt.
- `-s`, `--status`: Hiển thị trạng thái của một gói cụ thể.
- `-P`, `--purge`: Gỡ bỏ gói cùng với các file cấu hình.

## Common Examples
- Cài đặt một gói từ file `.deb`:
  ```bash
  dpkg -i package.deb
  ```
- Gỡ bỏ một gói đã cài đặt:
  ```bash
  dpkg -r package_name
  ```
- Liệt kê tất cả các gói đã cài đặt:
  ```bash
  dpkg -l
  ```
- Kiểm tra trạng thái của một gói:
  ```bash
  dpkg -s package_name
  ```
- Gỡ bỏ một gói cùng với các file cấu hình:
  ```bash
  dpkg -P package_name
  ```

## Tips
- Sử dụng `dpkg` cùng với `apt` để quản lý gói hiệu quả hơn, vì `apt` có thể tự động xử lý các phụ thuộc.
- Khi cài đặt gói, nếu gặp lỗi về phụ thuộc, hãy chạy `apt-get install -f` để sửa chữa.
- Đảm bảo rằng bạn có quyền root hoặc sử dụng `sudo` khi thực hiện các thao tác cài đặt hoặc gỡ bỏ gói.