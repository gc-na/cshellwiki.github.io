# [Linux] Bash apt sử dụng: Quản lý gói phần mềm

## Overview
Lệnh `apt` là một công cụ quản lý gói trên các hệ điều hành dựa trên Debian, cho phép người dùng cài đặt, nâng cấp, và gỡ bỏ phần mềm một cách dễ dàng.

## Usage
Cú pháp cơ bản của lệnh `apt` như sau:
```
apt [options] [arguments]
```

## Common Options
- `update`: Cập nhật danh sách gói từ các kho lưu trữ.
- `upgrade`: Nâng cấp tất cả các gói đã cài đặt lên phiên bản mới nhất.
- `install`: Cài đặt một gói phần mềm mới.
- `remove`: Gỡ bỏ một gói phần mềm đã cài đặt.
- `search`: Tìm kiếm gói phần mềm trong kho lưu trữ.

## Common Examples
- Cập nhật danh sách gói:
  ```bash
  sudo apt update
  ```

- Nâng cấp tất cả các gói:
  ```bash
  sudo apt upgrade
  ```

- Cài đặt một gói phần mềm, ví dụ `curl`:
  ```bash
  sudo apt install curl
  ```

- Gỡ bỏ một gói phần mềm, ví dụ `curl`:
  ```bash
  sudo apt remove curl
  ```

- Tìm kiếm gói phần mềm, ví dụ `nginx`:
  ```bash
  apt search nginx
  ```

## Tips
- Luôn chạy `sudo apt update` trước khi cài đặt hoặc nâng cấp để đảm bảo bạn có danh sách gói mới nhất.
- Sử dụng `apt autoremove` để gỡ bỏ các gói không còn cần thiết sau khi gỡ bỏ phần mềm.
- Kiểm tra các gói có thể nâng cấp bằng cách sử dụng `apt list --upgradable`.