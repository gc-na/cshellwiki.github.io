# [Hệ điều hành] C Shell (csh) who: Xem danh sách người dùng đăng nhập

## Overview
Lệnh `who` trong C Shell (csh) được sử dụng để hiển thị danh sách những người dùng hiện đang đăng nhập vào hệ thống. Nó cung cấp thông tin về tên người dùng, terminal mà họ đang sử dụng, thời gian đăng nhập và địa chỉ IP hoặc tên máy chủ (nếu có).

## Usage
Cú pháp cơ bản của lệnh `who` như sau:

```
who [options] [arguments]
```

## Common Options
Dưới đây là một số tùy chọn phổ biến cho lệnh `who`:

- `-b`: Hiển thị thời gian khởi động của hệ thống.
- `-q`: Chỉ hiển thị danh sách tên người dùng và số lượng người dùng đang đăng nhập.
- `-H`: Hiển thị tiêu đề cột cho kết quả.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `who`:

1. Hiển thị danh sách tất cả người dùng đang đăng nhập:
   ```csh
   who
   ```

2. Hiển thị thời gian khởi động của hệ thống:
   ```csh
   who -b
   ```

3. Chỉ hiển thị danh sách tên người dùng và số lượng người dùng:
   ```csh
   who -q
   ```

4. Hiển thị danh sách người dùng với tiêu đề cột:
   ```csh
   who -H
   ```

## Tips
- Sử dụng lệnh `who` thường xuyên để theo dõi ai đang sử dụng hệ thống của bạn.
- Kết hợp với lệnh `grep` để tìm kiếm người dùng cụ thể:
  ```csh
  who | grep username
  ```
- Kiểm tra thời gian đăng nhập của người dùng để quản lý phiên làm việc hiệu quả hơn.