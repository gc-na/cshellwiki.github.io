# [Linux] Bash builtin `type`: Xác định loại lệnh

## Overview
Lệnh `type` trong Bash được sử dụng để xác định loại của một lệnh, có thể là một lệnh nội bộ (builtin), lệnh bên ngoài, alias, hoặc function. Điều này hữu ích để hiểu rõ hơn về cách mà Bash xử lý các lệnh mà bạn nhập vào.

## Usage
Cú pháp cơ bản của lệnh `type` như sau:

```bash
type [options] [command]
```

## Common Options
- `-t`: Chỉ hiển thị loại của lệnh mà không có thông tin bổ sung.
- `-a`: Hiển thị tất cả các vị trí mà lệnh được tìm thấy, bao gồm cả alias và functions.
- `-p`: Hiển thị đường dẫn đầy đủ đến lệnh nếu nó là một lệnh bên ngoài.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `type`:

1. Kiểm tra loại của một lệnh:
   ```bash
   type ls
   ```

2. Kiểm tra loại của một alias:
   ```bash
   alias ll='ls -l'
   type ll
   ```

3. Hiển thị tất cả các vị trí của một lệnh:
   ```bash
   type -a echo
   ```

4. Kiểm tra loại của một function:
   ```bash
   my_function() { echo "Hello, World!"; }
   type my_function
   ```

## Tips
- Sử dụng `type -t` để nhanh chóng xác định loại lệnh mà không cần thông tin bổ sung.
- Kết hợp với `alias` để quản lý các lệnh tùy chỉnh của bạn một cách hiệu quả.
- Kiểm tra loại lệnh trước khi sử dụng để tránh nhầm lẫn giữa các lệnh nội bộ và bên ngoài.