# [Linux] Bash blkid Cách sử dụng: Xác định thông tin về thiết bị lưu trữ

## Overview
Lệnh `blkid` được sử dụng để xác định và hiển thị thông tin về các thiết bị lưu trữ trên hệ thống. Nó cung cấp thông tin như UUID, loại hệ thống tệp và nhãn của các phân vùng.

## Usage
Cú pháp cơ bản của lệnh `blkid` như sau:
```
blkid [options] [arguments]
```

## Common Options
- `-o, --output`: Chỉ định định dạng đầu ra (ví dụ: `value`, `full`, `device`).
- `-s, --match-tag`: Lọc thông tin theo thẻ cụ thể (ví dụ: `UUID`, `TYPE`).
- `-p, --probe`: Thực hiện kiểm tra để xác định thông tin về thiết bị.
- `-h, --help`: Hiển thị hướng dẫn sử dụng và các tùy chọn có sẵn.

## Common Examples
- Hiển thị thông tin về tất cả các thiết bị lưu trữ:
  ```bash
  blkid
  ```

- Hiển thị thông tin chỉ về UUID của các thiết bị:
  ```bash
  blkid -s UUID
  ```

- Lọc và hiển thị loại hệ thống tệp của một thiết bị cụ thể:
  ```bash
  blkid -s TYPE /dev/sda1
  ```

- Xuất thông tin với định dạng giá trị:
  ```bash
  blkid -o value -s UUID /dev/sda1
  ```

## Tips
- Sử dụng `sudo` nếu bạn không có quyền truy cập vào một số thiết bị.
- Kiểm tra thường xuyên thông tin UUID để đảm bảo các thiết bị được nhận diện chính xác trong hệ thống.
- Kết hợp `blkid` với các lệnh khác như `grep` để lọc thông tin một cách hiệu quả hơn.