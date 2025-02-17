# [Linux] Bash lvs sử dụng: Hiển thị thông tin về Logical Volume

## Overview
Lệnh `lvs` được sử dụng để hiển thị thông tin về các Logical Volume trong hệ thống quản lý Logical Volume Manager (LVM). Nó cung cấp cái nhìn tổng quan về các volume, bao gồm kích thước, trạng thái và các thuộc tính khác.

## Usage
Cú pháp cơ bản của lệnh `lvs` như sau:
```
lvs [options] [arguments]
```

## Common Options
- `-o`: Chỉ định các trường thông tin cụ thể để hiển thị.
- `-a`: Hiển thị tất cả các Logical Volume, bao gồm cả những volume không hoạt động.
- `--units`: Chỉ định đơn vị hiển thị kích thước (ví dụ: m, g, t).
- `-h`: Hiển thị kích thước theo định dạng dễ đọc hơn (ví dụ: 1G thay vì 1073741824).

## Common Examples
- Hiển thị danh sách tất cả các Logical Volume:
  ```bash
  lvs
  ```

- Hiển thị thông tin chi tiết về các Logical Volume với các trường cụ thể:
  ```bash
  lvs -o +devices
  ```

- Hiển thị tất cả các Logical Volume, bao gồm cả những volume không hoạt động:
  ```bash
  lvs -a
  ```

- Hiển thị kích thước của các Logical Volume theo đơn vị dễ đọc:
  ```bash
  lvs -h
  ```

## Tips
- Sử dụng tùy chọn `-o` để tùy chỉnh thông tin hiển thị theo nhu cầu của bạn.
- Kết hợp với các lệnh khác như `grep` để lọc thông tin cụ thể từ đầu ra của `lvs`.
- Thường xuyên kiểm tra trạng thái của các Logical Volume để đảm bảo hệ thống của bạn hoạt động ổn định.