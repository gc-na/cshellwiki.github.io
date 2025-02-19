# [Hệ điều hành] C Shell (csh) stat: Lấy thông tin về tệp

## Overview
Lệnh `stat` trong C Shell (csh) được sử dụng để hiển thị thông tin chi tiết về một tệp hoặc thư mục, bao gồm kích thước, thời gian tạo, quyền truy cập và nhiều thông tin khác.

## Usage
Cú pháp cơ bản của lệnh `stat` như sau:
```
stat [options] [arguments]
```

## Common Options
- `-c FORMAT`: Tùy chỉnh định dạng đầu ra theo yêu cầu.
- `-f FORMAT`: Tương tự như `-c`, nhưng sử dụng định dạng riêng cho hệ thống tệp.
- `-L`: Theo dõi liên kết mềm và hiển thị thông tin của tệp mà nó trỏ tới.

## Common Examples
- Hiển thị thông tin chi tiết về một tệp cụ thể:
  ```csh
  stat filename.txt
  ```

- Sử dụng tùy chọn `-c` để chỉ định định dạng đầu ra:
  ```csh
  stat -c '%s bytes' filename.txt
  ```

- Hiển thị thông tin của một thư mục:
  ```csh
  stat /path/to/directory
  ```

- Theo dõi liên kết mềm:
  ```csh
  stat -L symlink
  ```

## Tips
- Sử dụng tùy chọn `-c` để tùy chỉnh thông tin đầu ra theo nhu cầu cụ thể của bạn.
- Kiểm tra quyền truy cập của tệp để đảm bảo bạn có quyền thực hiện các thao tác cần thiết.
- Kết hợp với các lệnh khác như `grep` để lọc thông tin đầu ra nếu cần thiết.