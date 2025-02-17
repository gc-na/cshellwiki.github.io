# [Linux] Bash chkconfig sử dụng: Quản lý dịch vụ khởi động

## Overview
Lệnh `chkconfig` được sử dụng để quản lý các dịch vụ khởi động trên hệ thống Linux. Nó cho phép người dùng bật hoặc tắt các dịch vụ để chúng tự động khởi động khi hệ thống khởi động.

## Usage
Cú pháp cơ bản của lệnh `chkconfig` như sau:
```bash
chkconfig [options] [arguments]
```

## Common Options
- `--list`: Liệt kê tất cả các dịch vụ và trạng thái của chúng.
- `--add`: Thêm một dịch vụ mới vào danh sách khởi động.
- `--del`: Xóa một dịch vụ khỏi danh sách khởi động.
- `--level`: Chỉ định cấp độ chạy mà dịch vụ sẽ được bật hoặc tắt.

## Common Examples
1. **Liệt kê tất cả các dịch vụ:**
   ```bash
   chkconfig --list
   ```

2. **Bật một dịch vụ:**
   ```bash
   chkconfig httpd on
   ```

3. **Tắt một dịch vụ:**
   ```bash
   chkconfig httpd off
   ```

4. **Thêm một dịch vụ mới:**
   ```bash
   chkconfig --add myservice
   ```

5. **Xóa một dịch vụ:**
   ```bash
   chkconfig --del myservice
   ```

## Tips
- Hãy kiểm tra trạng thái của dịch vụ sau khi bật hoặc tắt bằng cách sử dụng lệnh `service <tên dịch vụ> status`.
- Sử dụng `chkconfig --level 2345 <tên dịch vụ> on` để bật dịch vụ chỉ ở các cấp độ chạy cụ thể.
- Đảm bảo rằng bạn có quyền quản trị (root) khi thực hiện các thay đổi với `chkconfig`.