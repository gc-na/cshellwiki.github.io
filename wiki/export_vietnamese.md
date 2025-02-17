# [Linux] Bash export: Thiết lập biến môi trường

## Overview
Lệnh `export` trong Bash được sử dụng để thiết lập và xuất các biến môi trường, cho phép các biến này có thể được truy cập bởi các tiến trình con của shell. Khi một biến được xuất, nó trở thành một phần của môi trường của shell và có thể được sử dụng bởi các chương trình khác.

## Usage
Cú pháp cơ bản của lệnh `export` như sau:

```bash
export [options] [arguments]
```

## Common Options
- `-p`: Hiển thị danh sách tất cả các biến môi trường hiện có.
- `-n`: Hủy xuất một biến môi trường, làm cho nó không còn khả dụng cho các tiến trình con.
- `-f`: Xuất một hàm shell để có thể được sử dụng trong các shell con.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `export`:

1. **Xuất một biến môi trường:**
   ```bash
   export MY_VAR="Hello World"
   ```

2. **Kiểm tra biến môi trường đã xuất:**
   ```bash
   echo $MY_VAR
   ```

3. **Xuất nhiều biến cùng một lúc:**
   ```bash
   export VAR1="Value1" VAR2="Value2"
   ```

4. **Hủy xuất một biến môi trường:**
   ```bash
   export -n MY_VAR
   ```

5. **Xuất một hàm shell:**
   ```bash
   my_function() {
       echo "This is a function"
   }
   export -f my_function
   ```

## Tips
- Hãy nhớ rằng các biến môi trường chỉ có thể được truy cập bởi các tiến trình con sau khi chúng được xuất.
- Sử dụng `export -p` để xem tất cả các biến môi trường hiện tại, điều này có thể hữu ích để kiểm tra các biến đã được thiết lập.
- Đặt các biến môi trường trong tệp cấu hình như `.bashrc` hoặc `.bash_profile` để chúng có hiệu lực mỗi khi bạn mở một phiên làm việc mới.