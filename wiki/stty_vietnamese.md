# [Hệ điều hành] C Shell (csh) stty: Thiết lập và kiểm soát các thuộc tính của terminal

## Overview
Lệnh `stty` trong C Shell (csh) được sử dụng để thay đổi và kiểm soát các thuộc tính của terminal. Nó cho phép người dùng cấu hình các thiết lập như chế độ nhập liệu, chế độ xuất, và các thông số khác liên quan đến cách mà terminal hoạt động.

## Usage
Cú pháp cơ bản của lệnh `stty` như sau:
```csh
stty [options] [arguments]
```

## Common Options
Dưới đây là một số tùy chọn phổ biến của lệnh `stty` cùng với giải thích ngắn gọn:

- `-a`: Hiển thị tất cả các thiết lập hiện tại của terminal.
- `-g`: Xuất các thiết lập hiện tại dưới dạng một chuỗi có thể sử dụng lại.
- `erase <char>`: Thiết lập ký tự xóa (thường là Backspace).
- `kill <char>`: Thiết lập ký tự để xóa dòng (thường là Ctrl + U).
- `intr <char>`: Thiết lập ký tự để ngắt (thường là Ctrl + C).
- `sane`: Đặt lại terminal về trạng thái mặc định.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `stty`:

1. Hiển thị tất cả các thiết lập hiện tại của terminal:
   ```csh
   stty -a
   ```

2. Thiết lập ký tự xóa là Backspace:
   ```csh
   stty erase ^H
   ```

3. Thiết lập ký tự ngắt là Ctrl + C:
   ```csh
   stty intr ^C
   ```

4. Đặt lại terminal về trạng thái mặc định:
   ```csh
   stty sane
   ```

5. Xuất các thiết lập hiện tại để sử dụng lại:
   ```csh
   stty -g
   ```

## Tips
- Hãy cẩn thận khi thay đổi các thiết lập của terminal, vì một số thay đổi có thể ảnh hưởng đến cách bạn tương tác với hệ thống.
- Sử dụng `stty -a` để kiểm tra các thiết lập hiện tại trước khi thực hiện bất kỳ thay đổi nào.
- Nếu bạn không chắc chắn về một tùy chọn, hãy tham khảo tài liệu hoặc sử dụng `man stty` để biết thêm thông tin.