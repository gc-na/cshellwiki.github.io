# [Linux] Bash stty cách sử dụng: Thiết lập và kiểm soát chế độ đầu vào/đầu ra

## Tổng quan
Lệnh `stty` trong Bash được sử dụng để thay đổi và kiểm soát các thuộc tính của terminal, bao gồm các thiết lập đầu vào và đầu ra. Nó cho phép người dùng tùy chỉnh cách mà terminal xử lý các ký tự và tín hiệu.

## Cách sử dụng
Cú pháp cơ bản của lệnh `stty` như sau:
```bash
stty [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`: Hiển thị tất cả các thiết lập hiện tại của terminal.
- `-g`: Xuất các thiết lập hiện tại dưới dạng một chuỗi có thể sử dụng lại.
- `erase <char>`: Đặt ký tự xóa (thường là phím Backspace).
- `kill <char>`: Đặt ký tự xóa dòng (thường là phím Ctrl + U).
- `-echo`: Tắt hiển thị ký tự khi gõ trên terminal.
- `echo`: Bật hiển thị ký tự khi gõ trên terminal.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `stty`:

1. **Hiển thị tất cả các thiết lập hiện tại:**
   ```bash
   stty -a
   ```

2. **Đặt ký tự xóa là phím Backspace:**
   ```bash
   stty erase ^H
   ```

3. **Tắt hiển thị ký tự khi gõ:**
   ```bash
   stty -echo
   ```

4. **Bật lại hiển thị ký tự khi gõ:**
   ```bash
   stty echo
   ```

5. **Xuất các thiết lập hiện tại dưới dạng chuỗi:**
   ```bash
   stty -g
   ```

## Mẹo
- Hãy cẩn thận khi sử dụng tùy chọn `-echo`, vì nó sẽ không cho phép bạn thấy các ký tự bạn đang gõ, có thể gây khó khăn trong việc nhập lệnh.
- Nếu bạn muốn khôi phục các thiết lập mặc định của terminal, bạn có thể sử dụng lệnh `stty sane`.
- Sử dụng `stty -a` để kiểm tra các thiết lập hiện tại trước khi thực hiện bất kỳ thay đổi nào, giúp bạn hiểu rõ hơn về trạng thái của terminal.