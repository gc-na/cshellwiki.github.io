# [Linux] Bash sftp cách sử dụng: Truy cập và truyền tệp an toàn qua SSH

## Tổng quan
Lệnh `sftp` (SSH File Transfer Protocol) cho phép người dùng truyền tệp giữa máy cục bộ và máy chủ từ xa một cách an toàn thông qua giao thức SSH. Đây là một công cụ hữu ích cho việc quản lý và chuyển đổi tệp trên các hệ thống khác nhau.

## Cách sử dụng
Cú pháp cơ bản của lệnh `sftp` như sau:

```bash
sftp [options] [user@]host
```

## Các tùy chọn phổ biến
- `-P port`: Chỉ định cổng để kết nối (mặc định là 22).
- `-i identity_file`: Sử dụng tệp khóa riêng để xác thực.
- `-o option`: Chỉ định tùy chọn cho SSH.
- `-v`: Bật chế độ chi tiết để hiển thị thông tin kết nối.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `sftp`:

1. Kết nối đến máy chủ từ xa:
   ```bash
   sftp user@hostname
   ```

2. Chuyển tệp từ máy cục bộ lên máy chủ:
   ```bash
   sftp user@hostname
   put localfile.txt
   ```

3. Tải tệp từ máy chủ về máy cục bộ:
   ```bash
   sftp user@hostname
   get remotefile.txt
   ```

4. Chuyển đổi thư mục từ máy cục bộ lên máy chủ:
   ```bash
   sftp user@hostname
   put -r localdirectory/
   ```

5. Liệt kê các tệp trong thư mục từ xa:
   ```bash
   sftp user@hostname
   ls
   ```

## Mẹo
- Hãy chắc chắn rằng bạn đã thiết lập đúng quyền truy cập và xác thực trên máy chủ từ xa để tránh gặp phải các lỗi khi kết nối.
- Sử dụng chế độ chi tiết (`-v`) để gỡ lỗi nếu bạn gặp vấn đề khi kết nối hoặc truyền tệp.
- Thường xuyên kiểm tra và dọn dẹp các tệp không cần thiết trên máy chủ để tiết kiệm không gian lưu trữ.