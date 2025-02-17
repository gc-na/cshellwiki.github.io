# [Linux] Bash pvs Cách sử dụng: Hiển thị thông tin về các volume trong LVM

## Overview
Lệnh `pvs` được sử dụng để hiển thị thông tin về các volume vật lý trong Logical Volume Manager (LVM). Nó cho phép người dùng xem các thuộc tính của các volume vật lý, giúp quản lý và theo dõi các tài nguyên lưu trữ hiệu quả hơn.

## Usage
Cú pháp cơ bản của lệnh `pvs` như sau:
```
pvs [options] [arguments]
```

## Common Options
- `-o, --options`: Chỉ định các cột thông tin nào sẽ được hiển thị.
- `-f, --full`: Hiển thị thông tin đầy đủ về các volume.
- `--units`: Chỉ định đơn vị hiển thị cho kích thước.
- `-d, --debug`: Bật chế độ gỡ lỗi để hiển thị thông tin chi tiết hơn.

## Common Examples
- Hiển thị danh sách tất cả các volume vật lý:
  ```bash
  pvs
  ```

- Hiển thị thông tin đầy đủ về các volume vật lý:
  ```bash
  pvs -f
  ```

- Hiển thị thông tin với các cột tùy chỉnh:
  ```bash
  pvs -o +pv_size,pv_free
  ```

- Hiển thị thông tin với đơn vị cụ thể:
  ```bash
  pvs --units g
  ```

## Tips
- Sử dụng tùy chọn `-o` để tùy chỉnh thông tin hiển thị, giúp bạn chỉ xem những gì cần thiết.
- Kết hợp `pvs` với các lệnh khác trong LVM như `lvdisplay` hoặc `vgdisplay` để có cái nhìn tổng thể về hệ thống lưu trữ của bạn.
- Thường xuyên kiểm tra các volume vật lý để đảm bảo rằng không có vấn đề nào xảy ra với lưu trữ của bạn.