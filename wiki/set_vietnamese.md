# [Linux] Bash set lệnh: Thiết lập các biến và tùy chọn trong shell

## Overview
Lệnh `set` trong Bash được sử dụng để thiết lập các biến và tùy chọn cho shell. Nó cho phép người dùng điều chỉnh hành vi của shell và quản lý các biến môi trường.

## Usage
Cú pháp cơ bản của lệnh `set` như sau:

```bash
set [options] [arguments]
```

## Common Options
Dưới đây là một số tùy chọn phổ biến của lệnh `set`:

- `-e`: Dừng thực thi nếu có lệnh nào đó trả về mã lỗi khác 0.
- `-u`: Báo lỗi khi sử dụng biến chưa được khởi tạo.
- `-x`: Hiển thị các lệnh được thực thi, hữu ích cho việc gỡ lỗi.
- `-o`: Thiết lập các tùy chọn khác cho shell, ví dụ `-o noclobber` để ngăn không cho ghi đè lên tệp.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `set`:

1. **Dừng thực thi khi có lỗi**:
   ```bash
   set -e
   command1
   command2  # Nếu command1 thất bại, command2 sẽ không được thực thi.
   ```

2. **Báo lỗi khi sử dụng biến chưa được khởi tạo**:
   ```bash
   set -u
   echo $my_var  # Sẽ báo lỗi nếu my_var chưa được khởi tạo.
   ```

3. **Hiển thị các lệnh đang được thực thi**:
   ```bash
   set -x
   echo "Hello, World!"  # Sẽ hiển thị lệnh này trước khi thực thi.
   ```

4. **Ngăn không cho ghi đè lên tệp**:
   ```bash
   set -o noclobber
   echo "Hello" > file.txt  # Sẽ tạo file.txt nếu chưa tồn tại, nhưng sẽ báo lỗi nếu file.txt đã tồn tại.
   ```

## Tips
- Sử dụng `set -e` để đảm bảo rằng script của bạn dừng lại khi có lỗi, giúp tránh các vấn đề không mong muốn.
- Kết hợp `set -u` và `set -e` để có một môi trường thực thi an toàn hơn.
- Sử dụng `set -x` trong quá trình gỡ lỗi để theo dõi các lệnh được thực thi và dễ dàng phát hiện lỗi.