# [Linux] Bash write sử dụng: Gửi tin nhắn đến người dùng khác

## Overview
Lệnh `write` cho phép người dùng gửi tin nhắn trực tiếp đến một người dùng khác đang đăng nhập trên cùng một hệ thống. Điều này rất hữu ích trong môi trường làm việc hoặc khi bạn cần giao tiếp nhanh chóng với đồng nghiệp.

## Usage
Cú pháp cơ bản của lệnh `write` như sau:
```
write [tên_người_dùng] [tên_tập_tin]
```

## Common Options
- `-n`: Không hiển thị thông báo khi bắt đầu gửi tin nhắn.
- `-s`: Gửi tin nhắn mà không hiển thị thông báo cho người nhận.

## Common Examples

Gửi tin nhắn đến người dùng có tên là `john`:
```bash
write john
```
Sau khi gõ lệnh này, bạn có thể nhập tin nhắn và nhấn `Ctrl+D` để gửi.

Gửi tin nhắn mà không hiển thị thông báo:
```bash
write -n john
```

Gửi tin nhắn từ một tập tin:
```bash
write john < message.txt
```

## Tips
- Đảm bảo rằng người nhận đang đăng nhập và có thể nhận tin nhắn.
- Sử dụng lệnh `who` để kiểm tra ai đang đăng nhập trên hệ thống trước khi gửi tin nhắn.
- Hãy nhớ rằng tin nhắn sẽ hiển thị trên màn hình của người nhận, vì vậy hãy cẩn thận với nội dung bạn gửi.