# [Linux] Bash talk cách sử dụng: Giao tiếp với người dùng khác

## Overview
Lệnh `talk` trong Bash cho phép người dùng giao tiếp trực tiếp với nhau trên cùng một hệ thống hoặc qua mạng. Nó mở một phiên trò chuyện hai chiều giữa hai người dùng, giúp họ có thể trao đổi thông tin một cách nhanh chóng và hiệu quả.

## Usage
Cú pháp cơ bản của lệnh `talk` như sau:
```
talk [options] [user]@[host]
```

## Common Options
- `-a`: Cho phép gửi thông báo đến người dùng ngay cả khi họ đang không đăng nhập.
- `-m`: Sử dụng chế độ "m" để gửi tin nhắn mà không cần mở một cửa sổ trò chuyện.
- `-s`: Chỉ định chế độ "silent", không hiển thị thông báo khi người dùng nhận được tin nhắn.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `talk`:

1. Gửi tin nhắn đến người dùng trên cùng một máy:
   ```bash
   talk user1
   ```

2. Gửi tin nhắn đến người dùng trên một máy khác:
   ```bash
   talk user2@192.168.1.10
   ```

3. Sử dụng tùy chọn `-a` để gửi thông báo đến người dùng không đăng nhập:
   ```bash
   talk -a user3
   ```

4. Gửi tin nhắn mà không mở cửa sổ trò chuyện:
   ```bash
   talk -m user4
   ```

## Tips
- Đảm bảo rằng người nhận đang sẵn sàng để nhận tin nhắn trước khi gửi, vì lệnh `talk` sẽ mở một phiên trò chuyện mới.
- Kiểm tra xem người dùng có đang trực tuyến hay không bằng cách sử dụng lệnh `who`.
- Sử dụng lệnh `mesg n` để ngăn không cho người khác gửi tin nhắn đến bạn nếu bạn không muốn bị làm phiền.