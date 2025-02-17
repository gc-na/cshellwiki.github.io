# [Linux] Bash cp Cách sử dụng: Sao chép tệp và thư mục

## Overview
Lệnh `cp` trong Bash được sử dụng để sao chép tệp và thư mục từ vị trí này sang vị trí khác. Đây là một công cụ rất hữu ích trong việc quản lý tệp trên hệ thống.

## Usage
Cú pháp cơ bản của lệnh `cp` như sau:

```bash
cp [options] [arguments]
```

## Common Options
Dưới đây là một số tùy chọn phổ biến của lệnh `cp`:

- `-r`: Sao chép thư mục và tất cả các tệp con bên trong.
- `-i`: Yêu cầu xác nhận trước khi ghi đè lên tệp đã tồn tại.
- `-u`: Sao chép chỉ khi tệp nguồn mới hơn tệp đích hoặc tệp đích không tồn tại.
- `-v`: Hiển thị thông tin chi tiết về các tệp đang được sao chép.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `cp`:

1. Sao chép một tệp đơn giản:
   ```bash
   cp file1.txt file2.txt
   ```

2. Sao chép một thư mục cùng với tất cả các tệp con:
   ```bash
   cp -r myfolder/ myfolder_backup/
   ```

3. Sao chép tệp và yêu cầu xác nhận trước khi ghi đè:
   ```bash
   cp -i file1.txt file2.txt
   ```

4. Sao chép tệp chỉ khi tệp nguồn mới hơn tệp đích:
   ```bash
   cp -u file1.txt file2.txt
   ```

5. Hiển thị thông tin chi tiết khi sao chép:
   ```bash
   cp -v file1.txt file2.txt
   ```

## Tips
- Luôn kiểm tra tệp đích trước khi sao chép để tránh ghi đè dữ liệu quan trọng.
- Sử dụng tùy chọn `-i` để bảo vệ dữ liệu của bạn khỏi việc ghi đè không mong muốn.
- Khi sao chép thư mục lớn, hãy sử dụng tùy chọn `-v` để theo dõi tiến trình sao chép.