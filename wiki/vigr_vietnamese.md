# [Linux] Bash vigr Cách sử dụng: Chỉnh sửa tệp cấu hình vi

## Overview
Lệnh `vigr` được sử dụng để chỉnh sửa các tệp cấu hình hệ thống như `/etc/passwd` và `/etc/group` bằng trình soạn thảo văn bản `vi`. Lệnh này đảm bảo rằng tệp được khóa trong quá trình chỉnh sửa, giúp tránh xung đột khi nhiều người dùng cố gắng chỉnh sửa cùng một tệp.

## Usage
Cú pháp cơ bản của lệnh `vigr` như sau:
```
vigr [options] [arguments]
```

## Common Options
- `-h`, `--help`: Hiển thị hướng dẫn sử dụng.
- `-o`, `--editor`: Chỉ định trình soạn thảo khác để sử dụng thay vì `vi`.
- `-s`, `--silent`: Chạy lệnh mà không hiển thị thông báo.

## Common Examples
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `vigr`:

1. Mở tệp `/etc/passwd` để chỉnh sửa:
   ```bash
   vigr /etc/passwd
   ```

2. Mở tệp `/etc/group` với trình soạn thảo `nano` thay vì `vi`:
   ```bash
   vigr -o nano /etc/group
   ```

3. Hiển thị hướng dẫn sử dụng lệnh `vigr`:
   ```bash
   vigr --help
   ```

## Tips
- Luôn sao lưu tệp cấu hình trước khi chỉnh sửa để tránh mất dữ liệu.
- Sử dụng lệnh `vigr` thay vì `vi` khi chỉnh sửa các tệp cấu hình quan trọng để đảm bảo an toàn.
- Nếu bạn không quen với `vi`, hãy chỉ định trình soạn thảo khác mà bạn thoải mái hơn để sử dụng.