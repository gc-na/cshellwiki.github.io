# [Linux] Bash env cách sử dụng: [quản lý biến môi trường]

## Tổng quan
Lệnh `env` trong Bash được sử dụng để hiển thị hoặc thiết lập các biến môi trường. Nó cho phép người dùng chạy một chương trình trong một môi trường đã được điều chỉnh mà không cần thay đổi môi trường hiện tại của shell.

## Cách sử dụng
Cú pháp cơ bản của lệnh `env` như sau:
```
env [options] [arguments]
```

## Các tùy chọn phổ biến
- `-i`: Khởi tạo một môi trường trống, không có biến môi trường nào.
- `-u NAME`: Xóa biến môi trường có tên là `NAME`.
- `VAR=value`: Thiết lập một biến môi trường mới với giá trị `value`.

## Ví dụ thường gặp
1. **Hiển thị tất cả các biến môi trường**:
   ```bash
   env
   ```

2. **Chạy một chương trình với biến môi trường cụ thể**:
   ```bash
   env VAR1=value1 VAR2=value2 ./my_script.sh
   ```

3. **Xóa một biến môi trường trước khi chạy chương trình**:
   ```bash
   env -u VAR1 ./my_script.sh
   ```

4. **Khởi tạo môi trường trống**:
   ```bash
   env -i bash
   ```

## Mẹo
- Sử dụng `env` để kiểm tra các biến môi trường hiện tại trước khi thực hiện các thay đổi.
- Khi chạy các script, hãy sử dụng `env` để đảm bảo rằng các biến môi trường cần thiết được thiết lập đúng cách.
- Kết hợp `env` với các lệnh khác để tạo ra các môi trường tùy chỉnh cho các tác vụ cụ thể.