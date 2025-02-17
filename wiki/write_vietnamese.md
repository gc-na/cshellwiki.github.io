# [Linux] Bash write lệnh: Gửi tin nhắn đến người dùng khác

## Overview
Lệnh `write` trong Bash cho phép người dùng gửi tin nhắn trực tiếp đến một người dùng khác đang đăng nhập trên cùng một hệ thống. Đây là một cách hiệu quả để giao tiếp nhanh chóng trong môi trường nhiều người dùng.

## Usage
Cú pháp cơ bản của lệnh `write` như sau:

```
write [tên_người_dùng] [tên_tập_tin]
```

## Common Options
- `-n`: Không hiển thị tên người gửi.
- `-s`: Gửi tin nhắn mà không hiển thị thông báo đến người nhận.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `write`:

1. Gửi tin nhắn đến người dùng có tên là "user1":
   ```bash
   write user1
   ```
   Sau khi nhập lệnh, bạn có thể gõ tin nhắn và nhấn `Ctrl+D` để gửi.

2. Gửi tin nhắn mà không hiển thị tên người gửi:
   ```bash
   write -n user1
   ```

3. Gửi tin nhắn từ một tập tin:
   ```bash
   write user1 < message.txt
   ```

## Tips
- Đảm bảo rằng người nhận đang đăng nhập và không tắt tính năng nhận tin nhắn.
- Sử dụng lệnh `mesg` để kiểm tra hoặc thay đổi trạng thái nhận tin nhắn của bạn.
- Hãy nhớ rằng tin nhắn sẽ không được gửi nếu người nhận đã tắt tính năng nhận tin nhắn.