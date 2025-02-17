# [Linux] Bash complete: Tự động hoàn thành lệnh

## Tổng quan
Lệnh `complete` trong Bash được sử dụng để xác định cách mà các lệnh sẽ được tự động hoàn thành khi người dùng gõ. Nó cho phép bạn tùy chỉnh các tùy chọn hoàn thành cho các lệnh cụ thể, giúp tiết kiệm thời gian và giảm thiểu lỗi khi nhập lệnh.

## Cú pháp
Cú pháp cơ bản của lệnh `complete` như sau:
```bash
complete [options] [arguments]
```

## Các tùy chọn phổ biến
- `-A`: Xác định loại đối tượng mà lệnh sẽ hoàn thành (ví dụ: file, directory).
- `-F`: Chỉ định một hàm để xử lý việc hoàn thành.
- `-o`: Thêm các tùy chọn hoàn thành bổ sung.
- `-p`: Hiển thị các hoàn thành hiện tại cho một lệnh cụ thể.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `complete`:

1. **Hoàn thành tên file**:
   ```bash
   complete -A file mycommand
   ```
   Lệnh này sẽ cho phép `mycommand` hoàn thành tên file khi bạn gõ.

2. **Sử dụng hàm hoàn thành**:
   ```bash
   _my_custom_completion() {
       local options="option1 option2 option3"
       COMPREPLY=( $(compgen -W "$options" -- "${COMP_WORDS[COMP_CWORD]}") )
   }
   complete -F _my_custom_completion mycommand
   ```
   Trong ví dụ này, `mycommand` sẽ hoàn thành với các tùy chọn được định nghĩa trong hàm `_my_custom_completion`.

3. **Hoàn thành cho các lệnh đã được định nghĩa**:
   ```bash
   complete -o nospace -o filenames mycommand
   ```
   Lệnh này cho phép `mycommand` hoàn thành với tên file và không thêm khoảng trắng sau khi hoàn thành.

## Mẹo
- Hãy chắc chắn rằng bạn đã định nghĩa các hàm hoàn thành một cách rõ ràng để tránh nhầm lẫn cho người dùng.
- Kiểm tra các tùy chọn hoàn thành hiện tại bằng cách sử dụng `complete -p <command>` để xem các tùy chọn đã được thiết lập.
- Sử dụng lệnh `compgen` để tạo danh sách các tùy chọn hoàn thành một cách linh hoạt và hiệu quả.