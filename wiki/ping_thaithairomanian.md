# [Bash] ping sử dụng: Kiểm tra kết nối mạng

## Overview
Lệnh `ping` được sử dụng để kiểm tra kết nối mạng giữa máy tính của bạn và một địa chỉ IP hoặc tên miền. Nó gửi các gói tin ICMP Echo Request đến địa chỉ đích và chờ nhận phản hồi, giúp xác định xem địa chỉ đó có khả dụng hay không.

## Usage
Cú pháp cơ bản của lệnh `ping` như sau:
```
ping [options] [arguments]
```

## Common Options
- `-c [count]`: Chỉ định số lượng gói tin sẽ được gửi.
- `-i [interval]`: Đặt khoảng thời gian (giây) giữa các gói tin.
- `-t [ttl]`: Đặt giá trị Time To Live cho gói tin.
- `-s [size]`: Chỉ định kích thước của gói tin gửi đi.

## Common Examples
- Kiểm tra kết nối đến google.com:
  ```bash
  ping google.com
  ```

- Gửi 5 gói tin đến địa chỉ IP 8.8.8.8:
  ```bash
  ping -c 5 8.8.8.8
  ```

- Gửi gói tin với kích thước 100 bytes:
  ```bash
  ping -s 100 google.com
  ```

- Gửi gói tin với khoảng thời gian 2 giây giữa các gói:
  ```bash
  ping -i 2 google.com
  ```

## Tips
- Sử dụng tùy chọn `-c` để giới hạn số lượng gói tin, tránh việc gửi liên tục không cần thiết.
- Kiểm tra địa chỉ IP nội bộ để xác định vấn đề mạng trong hệ thống của bạn.
- Kết hợp `ping` với các lệnh khác như `grep` để lọc kết quả, ví dụ: `ping google.com | grep 'bytes from'`.