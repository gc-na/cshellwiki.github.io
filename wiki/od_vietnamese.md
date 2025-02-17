# [Linux] Bash od cách sử dụng: Hiển thị nội dung tệp ở định dạng khác nhau

## Overview
Lệnh `od` (octal dump) trong Bash được sử dụng để hiển thị nội dung của tệp ở nhiều định dạng khác nhau, bao gồm octal, hex, và ASCII. Điều này hữu ích cho việc phân tích tệp nhị phân hoặc kiểm tra dữ liệu không thể đọc được bằng văn bản thông thường.

## Usage
Cú pháp cơ bản của lệnh `od` như sau:
```
od [options] [arguments]
```

## Common Options
- `-A` : Chỉ định định dạng địa chỉ (ví dụ: `n` cho số thập phân, `o` cho số octal).
- `-t` : Chỉ định kiểu dữ liệu để hiển thị (ví dụ: `c` cho ký tự, `x` cho hex).
- `-N` : Chỉ định số byte tối đa để đọc từ tệp.
- `-v` : Hiển thị tất cả các byte, bao gồm cả các byte trống.

## Common Examples
- Hiển thị nội dung của tệp ở định dạng octal:
  ```bash
  od -c filename.txt
  ```

- Hiển thị nội dung của tệp ở định dạng hex:
  ```bash
  od -x filename.bin
  ```

- Hiển thị 16 byte đầu tiên của tệp:
  ```bash
  od -N 16 filename.txt
  ```

- Hiển thị địa chỉ và nội dung của tệp ở định dạng ASCII:
  ```bash
  od -A n -t a filename.txt
  ```

## Tips
- Sử dụng tùy chọn `-v` để đảm bảo bạn không bỏ lỡ bất kỳ byte nào trong tệp.
- Kết hợp các tùy chọn để tùy chỉnh đầu ra theo nhu cầu của bạn, ví dụ: `od -A n -t x -N 32 filename.bin` để xem 32 byte đầu tiên ở định dạng hex mà không có địa chỉ.
- Thử nghiệm với các định dạng khác nhau để hiểu rõ hơn về cấu trúc của tệp nhị phân.