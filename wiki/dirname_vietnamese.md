# [Hệ điều hành] C Shell (csh) dirname Cách sử dụng: Lấy tên thư mục từ đường dẫn

## Overview
Lệnh `dirname` trong C Shell (csh) được sử dụng để trích xuất tên thư mục từ một đường dẫn đầy đủ. Nó giúp người dùng dễ dàng lấy phần thư mục của một đường dẫn mà không cần phải xử lý thủ công.

## Usage
Cú pháp cơ bản của lệnh `dirname` như sau:
```
dirname [options] [arguments]
```

## Common Options
- `-z`: Chỉ định rằng đầu vào là một chuỗi rỗng.
- `--help`: Hiển thị thông tin trợ giúp về lệnh.
- `--version`: Hiển thị phiên bản của lệnh `dirname`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `dirname`:

1. Lấy tên thư mục từ một đường dẫn đầy đủ:
   ```csh
   dirname /home/user/documents/file.txt
   ```
   Kết quả: `/home/user/documents`

2. Lấy tên thư mục từ một đường dẫn tương đối:
   ```csh
   dirname ./projects/coding/script.sh
   ```
   Kết quả: `./projects/coding`

3. Sử dụng với nhiều đường dẫn:
   ```csh
   dirname /var/log/syslog /usr/local/bin/script.sh
   ```
   Kết quả:
   ```
   /var/log
   /usr/local/bin
   ```

## Tips
- Khi làm việc với nhiều đường dẫn, bạn có thể sử dụng `dirname` trong một vòng lặp để xử lý từng đường dẫn một cách tự động.
- Kết hợp `dirname` với các lệnh khác như `basename` có thể giúp bạn dễ dàng quản lý và xử lý các đường dẫn tệp tin trong shell.