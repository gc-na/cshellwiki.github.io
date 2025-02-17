# [Linux] Bash pkg sử dụng: Quản lý gói phần mềm

## Overview
Lệnh `pkg` được sử dụng để quản lý các gói phần mềm trên hệ thống. Nó cho phép người dùng cài đặt, gỡ bỏ, và cập nhật các gói phần mềm một cách dễ dàng.

## Usage
Cú pháp cơ bản của lệnh `pkg` như sau:

```
pkg [options] [arguments]
```

## Common Options
- `install`: Cài đặt một gói phần mềm.
- `remove`: Gỡ bỏ một gói phần mềm.
- `update`: Cập nhật danh sách các gói phần mềm.
- `upgrade`: Nâng cấp tất cả các gói phần mềm đã cài đặt lên phiên bản mới nhất.
- `search`: Tìm kiếm một gói phần mềm trong kho lưu trữ.

## Common Examples
- Cài đặt một gói phần mềm:
  ```bash
  pkg install tên-gói
  ```

- Gỡ bỏ một gói phần mềm:
  ```bash
  pkg remove tên-gói
  ```

- Cập nhật danh sách các gói phần mềm:
  ```bash
  pkg update
  ```

- Nâng cấp tất cả các gói phần mềm:
  ```bash
  pkg upgrade
  ```

- Tìm kiếm một gói phần mềm:
  ```bash
  pkg search tên-gói
  ```

## Tips
- Luôn cập nhật danh sách gói trước khi cài đặt hoặc nâng cấp để đảm bảo bạn có phiên bản mới nhất.
- Sử dụng `pkg search` để tìm kiếm gói phần mềm nếu bạn không chắc chắn về tên chính xác của nó.
- Kiểm tra các phụ thuộc của gói trước khi cài đặt để tránh xung đột phần mềm.