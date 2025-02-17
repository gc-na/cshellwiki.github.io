# [Linux] Bash telnet cách sử dụng: Kết nối tới máy chủ từ xa

## Tổng quan
Lệnh `telnet` được sử dụng để kết nối tới máy chủ từ xa qua giao thức Telnet. Nó cho phép người dùng gửi lệnh và nhận phản hồi từ máy chủ, thường được sử dụng để kiểm tra kết nối mạng hoặc quản lý thiết bị mạng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `telnet` như sau:

```bash
telnet [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-l [tên người dùng]`: Đăng nhập với tên người dùng cụ thể.
- `-n [tên tệp]`: Ghi lại phiên làm việc vào tệp.
- `-f [tên tệp]`: Nhận dữ liệu từ tệp.
- `-e [ký tự]`: Đặt ký tự để thoát khỏi telnet.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `telnet`:

1. Kết nối tới một máy chủ trên cổng 23 (cổng mặc định của Telnet):
   ```bash
   telnet example.com
   ```

2. Kết nối tới một máy chủ trên cổng 80 (cổng HTTP):
   ```bash
   telnet example.com 80
   ```

3. Sử dụng tên người dùng cụ thể để đăng nhập:
   ```bash
   telnet -l username example.com
   ```

4. Ghi lại phiên làm việc vào tệp:
   ```bash
   telnet -n session.log example.com
   ```

## Mẹo
- Hãy chắc chắn rằng bạn có quyền truy cập vào máy chủ mà bạn đang cố gắng kết nối.
- Sử dụng `telnet` chủ yếu cho mục đích kiểm tra kết nối, vì giao thức Telnet không mã hóa dữ liệu, có thể gây rủi ro bảo mật.
- Nếu bạn cần một kết nối an toàn hơn, hãy xem xét sử dụng SSH thay vì Telnet.