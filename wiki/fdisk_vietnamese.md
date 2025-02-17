# [Linux] Bash fdisk: Quản lý phân vùng ổ đĩa

## Overview
Lệnh `fdisk` là một công cụ mạnh mẽ trong Linux được sử dụng để quản lý các phân vùng trên ổ đĩa cứng. Nó cho phép người dùng tạo, xóa, thay đổi kích thước và kiểm tra các phân vùng, giúp tối ưu hóa việc sử dụng không gian lưu trữ.

## Usage
Cú pháp cơ bản của lệnh `fdisk` như sau:
```bash
fdisk [options] [arguments]
```

## Common Options
- `-l`: Liệt kê tất cả các phân vùng trên tất cả các ổ đĩa.
- `-u`: Hiển thị kích thước phân vùng bằng đơn vị sector.
- `-s`: Hiển thị kích thước của một phân vùng cụ thể.
- `-n`: Tạo một phân vùng mới.
- `-d`: Xóa một phân vùng.

## Common Examples
1. **Liệt kê các phân vùng trên ổ đĩa**:
   ```bash
   fdisk -l
   ```

2. **Tạo một phân vùng mới**:
   ```bash
   fdisk /dev/sda
   ```
   Sau đó, bạn có thể nhập các lệnh tương ứng trong giao diện tương tác của `fdisk`.

3. **Xóa một phân vùng**:
   ```bash
   fdisk /dev/sda
   ```
   Trong giao diện tương tác, bạn có thể chọn phân vùng cần xóa và nhập lệnh thích hợp.

4. **Kiểm tra kích thước của một phân vùng**:
   ```bash
   fdisk -s /dev/sda1
   ```

## Tips
- Trước khi thực hiện bất kỳ thay đổi nào với `fdisk`, hãy sao lưu dữ liệu quan trọng để tránh mất mát.
- Sử dụng lệnh `man fdisk` để xem hướng dẫn chi tiết và các tùy chọn khác.
- Cẩn thận khi xóa hoặc thay đổi phân vùng, vì điều này có thể ảnh hưởng đến hệ thống và dữ liệu của bạn.