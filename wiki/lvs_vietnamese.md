# [Linux] Bash lvs: Hiển thị thông tin về các logical volume

## Overview
Lệnh `lvs` được sử dụng để hiển thị thông tin về các logical volume trong hệ thống Linux sử dụng LVM (Logical Volume Manager). Nó cung cấp cái nhìn tổng quan về các logical volume, bao gồm kích thước, trạng thái và các thuộc tính khác.

## Usage
Cú pháp cơ bản của lệnh `lvs` như sau:
```bash
lvs [options] [arguments]
```

## Common Options
- `-a`, `--all`: Hiển thị tất cả các logical volume, bao gồm cả những volume không hoạt động.
- `-o`, `--units`: Chỉ định các trường hiển thị và đơn vị kích thước.
- `-h`, `--help`: Hiển thị hướng dẫn sử dụng lệnh.
- `-o`, `--options`: Chỉ định các thuộc tính cụ thể cần hiển thị, ví dụ như `lv_size`, `lv_attr`.

## Common Examples
- Hiển thị danh sách tất cả các logical volume:
  ```bash
  lvs
  ```

- Hiển thị thông tin chi tiết về các logical volume, bao gồm kích thước và trạng thái:
  ```bash
  lvs -o +devices
  ```

- Hiển thị tất cả các logical volume, bao gồm cả những volume không hoạt động:
  ```bash
  lvs -a
  ```

- Hiển thị thông tin về logical volume với các thuộc tính cụ thể:
  ```bash
  lvs -o lv_name,lv_size,lv_attr
  ```

## Tips
- Sử dụng tùy chọn `-o` để tùy chỉnh thông tin hiển thị theo nhu cầu của bạn.
- Kết hợp lệnh `lvs` với các lệnh khác như `lvcreate`, `lvremove` để quản lý logical volume hiệu quả hơn.
- Thường xuyên kiểm tra trạng thái của các logical volume để đảm bảo hệ thống hoạt động ổn định.