# [Linux] Bash uptime Cách sử dụng: Kiểm tra thời gian hoạt động của hệ thống

## Overview
Lệnh `uptime` trong Bash được sử dụng để hiển thị thời gian mà hệ thống đã hoạt động liên tục kể từ lần khởi động gần nhất. Nó cung cấp thông tin về thời gian hoạt động, số lượng người dùng đang đăng nhập và tải trung bình của hệ thống trong 1, 5 và 15 phút qua.

## Usage
Cú pháp cơ bản của lệnh `uptime` như sau:
```
uptime [options]
```

## Common Options
- `-p`, `--pretty`: Hiển thị thời gian hoạt động theo cách dễ hiểu hơn.
- `-s`, `--since`: Hiển thị thời gian khởi động của hệ thống.

## Common Examples
- Hiển thị thời gian hoạt động của hệ thống:
  ```bash
  uptime
  ```

- Hiển thị thời gian hoạt động theo cách dễ hiểu:
  ```bash
  uptime -p
  ```

- Hiển thị thời gian khởi động của hệ thống:
  ```bash
  uptime -s
  ```

## Tips
- Sử dụng lệnh `uptime` để theo dõi hiệu suất của hệ thống, đặc biệt khi có nhiều người dùng cùng truy cập.
- Kết hợp lệnh `uptime` với các lệnh khác như `top` hoặc `htop` để có cái nhìn tổng quát hơn về tình trạng hệ thống.
- Thường xuyên kiểm tra thời gian hoạt động để phát hiện các vấn đề về hiệu suất hoặc sự cố không mong muốn.