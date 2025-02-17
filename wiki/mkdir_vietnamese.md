# [Linux] Bash mkdir Cách sử dụng: Tạo thư mục mới

## Overview
Lệnh `mkdir` trong Bash được sử dụng để tạo thư mục mới trong hệ thống tệp. Đây là một công cụ cơ bản nhưng rất hữu ích cho việc tổ chức và quản lý dữ liệu.

## Usage
Cú pháp cơ bản của lệnh `mkdir` như sau:
```
mkdir [options] [arguments]
```

## Common Options
- `-p`: Tạo các thư mục cha nếu chúng chưa tồn tại.
- `-v`: Hiển thị thông báo cho mỗi thư mục được tạo.
- `-m`: Đặt quyền truy cập cho thư mục mới.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mkdir`:

1. Tạo một thư mục mới đơn giản:
   ```bash
   mkdir myfolder
   ```

2. Tạo nhiều thư mục cùng một lúc:
   ```bash
   mkdir folder1 folder2 folder3
   ```

3. Tạo thư mục cha nếu chưa tồn tại:
   ```bash
   mkdir -p parent/child
   ```

4. Tạo thư mục mới và hiển thị thông báo:
   ```bash
   mkdir -v newfolder
   ```

5. Tạo thư mục với quyền truy cập cụ thể:
   ```bash
   mkdir -m 755 mysecurefolder
   ```

## Tips
- Sử dụng tùy chọn `-p` để tránh lỗi khi thư mục cha chưa tồn tại.
- Kiểm tra quyền truy cập của thư mục sau khi tạo để đảm bảo rằng bạn có quyền cần thiết.
- Đặt tên thư mục một cách rõ ràng và có tổ chức để dễ dàng quản lý sau này.