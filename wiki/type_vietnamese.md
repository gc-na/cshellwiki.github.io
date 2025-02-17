# [Linux] Bash type: Xác định loại của một lệnh

## Overview
Lệnh `type` trong Bash được sử dụng để xác định loại của một lệnh, cho biết liệu lệnh đó là một lệnh nội bộ, lệnh ngoại vi, hay một alias. Điều này rất hữu ích khi bạn muốn biết cách mà Bash sẽ xử lý một lệnh cụ thể.

## Usage
Cú pháp cơ bản của lệnh `type` như sau:

```bash
type [options] [arguments]
```

## Common Options
- `-a`: Hiển thị tất cả các vị trí mà lệnh được tìm thấy, bao gồm cả alias và lệnh nội bộ.
- `-p`: Chỉ hiển thị đường dẫn đầy đủ đến lệnh ngoại vi, nếu có.
- `-t`: Hiển thị loại của lệnh mà không cần thông tin bổ sung.

## Common Examples

1. **Kiểm tra loại lệnh**:
   ```bash
   type ls
   ```
   Kết quả sẽ cho biết `ls` là một lệnh ngoại vi.

2. **Xem tất cả các vị trí của lệnh**:
   ```bash
   type -a echo
   ```
   Kết quả sẽ hiển thị tất cả các alias và lệnh nội bộ liên quan đến `echo`.

3. **Kiểm tra loại của một alias**:
   ```bash
   alias ll='ls -l'
   type ll
   ```
   Kết quả sẽ cho biết `ll` là một alias.

4. **Chỉ hiển thị đường dẫn đến lệnh ngoại vi**:
   ```bash
   type -p grep
   ```
   Kết quả sẽ cho biết đường dẫn đầy đủ đến lệnh `grep`.

5. **Xem loại của một lệnh nội bộ**:
   ```bash
   type cd
   ```
   Kết quả sẽ cho biết `cd` là một lệnh nội bộ.

## Tips
- Sử dụng `type -a` để có cái nhìn tổng quát về tất cả các phiên bản của một lệnh, đặc biệt khi bạn có nhiều alias.
- Kiểm tra loại lệnh trước khi sử dụng để đảm bảo bạn đang gọi đúng lệnh mà bạn mong muốn.
- Kết hợp `type` với các lệnh khác để tạo ra các script tự động kiểm tra loại lệnh trong môi trường của bạn.