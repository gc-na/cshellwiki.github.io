# [Linux] Bash sleep sử dụng: Tạm dừng thực thi trong một khoảng thời gian

## Overview
Lệnh `sleep` trong Bash được sử dụng để tạm dừng thực thi của một script hoặc lệnh trong một khoảng thời gian nhất định. Điều này hữu ích khi bạn cần tạo khoảng cách giữa các lệnh hoặc khi bạn muốn trì hoãn một hành động nào đó.

## Usage
Cú pháp cơ bản của lệnh `sleep` như sau:
```bash
sleep [options] [arguments]
```

## Common Options
- `-h`, `--help`: Hiển thị thông tin trợ giúp về lệnh `sleep`.
- `-V`, `--version`: Hiển thị phiên bản của lệnh `sleep`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `sleep`:

1. Tạm dừng trong 5 giây:
   ```bash
   sleep 5
   ```

2. Tạm dừng trong 2 phút:
   ```bash
   sleep 2m
   ```

3. Tạm dừng trong 1 giờ:
   ```bash
   sleep 1h
   ```

4. Sử dụng trong một script để tạm dừng giữa các lệnh:
   ```bash
   echo "Bắt đầu..."
   sleep 3
   echo "Kết thúc sau 3 giây."
   ```

## Tips
- Sử dụng `sleep` để tạo khoảng thời gian giữa các lệnh trong một script để tránh quá tải hệ thống.
- Kết hợp `sleep` với các lệnh khác trong một vòng lặp để thực hiện các tác vụ định kỳ.
- Hãy nhớ rằng thời gian có thể được chỉ định bằng giây (s), phút (m), giờ (h) hoặc ngày (d).