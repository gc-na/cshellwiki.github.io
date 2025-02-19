# [Hệ điều hành] C Shell (csh) du: Đo kích thước thư mục

## Overview
Lệnh `du` (disk usage) trong C Shell được sử dụng để đo kích thước của các thư mục và tệp tin trong hệ thống. Nó giúp người dùng hiểu rõ hơn về không gian lưu trữ đang được sử dụng.

## Usage
Cú pháp cơ bản của lệnh `du` như sau:

```csh
du [options] [arguments]
```

## Common Options
- `-h`: Hiển thị kích thước theo định dạng dễ đọc (KB, MB, GB).
- `-s`: Tóm tắt kích thước của thư mục mà không hiển thị kích thước của các tệp con.
- `-a`: Hiển thị kích thước của tất cả các tệp và thư mục.
- `-c`: Tính tổng kích thước và hiển thị ở cuối danh sách.

## Common Examples
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `du`:

1. Đo kích thước của thư mục hiện tại:
   ```csh
   du
   ```

2. Đo kích thước của một thư mục cụ thể với định dạng dễ đọc:
   ```csh
   du -h /path/to/directory
   ```

3. Tóm tắt kích thước của một thư mục mà không hiển thị chi tiết:
   ```csh
   du -sh /path/to/directory
   ```

4. Hiển thị kích thước của tất cả các tệp và thư mục trong thư mục hiện tại:
   ```csh
   du -a
   ```

5. Tính tổng kích thước của các thư mục và hiển thị ở cuối:
   ```csh
   du -ch /path/to/directory/*
   ```

## Tips
- Sử dụng tùy chọn `-h` để dễ dàng đọc kích thước, đặc biệt khi làm việc với các thư mục lớn.
- Kết hợp `du` với lệnh `sort` để sắp xếp các thư mục theo kích thước:
  ```csh
  du -h | sort -hr
  ```
- Thường xuyên kiểm tra kích thước thư mục để quản lý không gian lưu trữ hiệu quả hơn.