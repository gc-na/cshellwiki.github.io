# [Linux] Bash ftp cách sử dụng: Giao thức truyền tệp

## Tổng quan
Lệnh `ftp` (File Transfer Protocol) được sử dụng để truyền tệp giữa máy tính của bạn và máy chủ FTP. Nó cho phép bạn tải lên, tải xuống và quản lý tệp trên máy chủ từ xa một cách dễ dàng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `ftp` như sau:
```
ftp [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-i`: Tắt chế độ tương tác, cho phép truyền tệp mà không cần xác nhận.
- `-v`: Hiển thị thông tin chi tiết về quá trình truyền tệp.
- `-n`: Ngăn không cho tự động kết nối đến máy chủ FTP.
- `-p`: Sử dụng chế độ truyền tệp chủ động.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `ftp`:

1. Kết nối đến máy chủ FTP:
   ```bash
   ftp ftp.example.com
   ```

2. Tải xuống một tệp từ máy chủ FTP:
   ```bash
   get filename.txt
   ```

3. Tải lên một tệp lên máy chủ FTP:
   ```bash
   put localfile.txt
   ```

4. Liệt kê các tệp trong thư mục hiện tại trên máy chủ FTP:
   ```bash
   ls
   ```

5. Thoát khỏi phiên làm việc FTP:
   ```bash
   bye
   ```

## Mẹo
- Hãy chắc chắn rằng bạn đã có quyền truy cập vào máy chủ FTP trước khi cố gắng kết nối.
- Sử dụng chế độ `-i` khi truyền nhiều tệp để tránh việc xác nhận từng tệp.
- Kiểm tra kết nối mạng của bạn nếu gặp sự cố khi kết nối đến máy chủ FTP.
- Để bảo mật hơn, hãy cân nhắc sử dụng `sftp` thay vì `ftp` để mã hóa dữ liệu trong quá trình truyền.