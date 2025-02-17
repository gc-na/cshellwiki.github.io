# [Linux] Bash top sử dụng: Hiển thị thông tin về tiến trình hệ thống

## Overview
Lệnh `top` trong Bash được sử dụng để hiển thị thông tin theo thời gian thực về các tiến trình đang chạy trên hệ thống. Nó cung cấp cái nhìn tổng quan về việc sử dụng CPU, bộ nhớ và các thông tin khác liên quan đến hiệu suất của hệ thống.

## Usage
Cú pháp cơ bản của lệnh `top` như sau:
```bash
top [options] [arguments]
```

## Common Options
- `-d <seconds>`: Đặt khoảng thời gian giữa các lần cập nhật thông tin.
- `-n <number>`: Chỉ định số lần cập nhật trước khi thoát.
- `-u <username>`: Hiển thị chỉ các tiến trình của người dùng cụ thể.
- `-p <pid>`: Theo dõi một tiến trình cụ thể theo ID tiến trình.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `top`:

1. Chạy lệnh `top` để xem thông tin về tất cả các tiến trình:
   ```bash
   top
   ```

2. Chạy `top` với khoảng thời gian cập nhật là 5 giây:
   ```bash
   top -d 5
   ```

3. Chỉ hiển thị các tiến trình của người dùng cụ thể:
   ```bash
   top -u username
   ```

4. Theo dõi một tiến trình cụ thể bằng ID tiến trình:
   ```bash
   top -p 1234
   ```

5. Chạy `top` và chỉ định số lần cập nhật là 10:
   ```bash
   top -n 10
   ```

## Tips
- Sử dụng phím `h` trong giao diện `top` để xem hướng dẫn sử dụng.
- Nhấn `Shift + M` để sắp xếp các tiến trình theo mức sử dụng bộ nhớ.
- Nhấn `Shift + P` để sắp xếp theo mức sử dụng CPU.
- Để thoát khỏi `top`, nhấn phím `q`.