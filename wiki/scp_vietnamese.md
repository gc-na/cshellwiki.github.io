# [Linux] Bash scp cách sử dụng: Chuyển file an toàn giữa các máy tính

## Tổng quan
Lệnh `scp` (Secure Copy Protocol) được sử dụng để sao chép file và thư mục giữa các máy tính qua mạng một cách an toàn. Nó sử dụng giao thức SSH để đảm bảo rằng dữ liệu được truyền tải một cách bảo mật.

## Cách sử dụng
Cú pháp cơ bản của lệnh `scp` như sau:
```
scp [options] [arguments]
```

## Các tùy chọn phổ biến
- `-r`: Sao chép thư mục và tất cả các file bên trong.
- `-P`: Chỉ định cổng SSH khác (mặc định là 22).
- `-i`: Chỉ định file khóa riêng để xác thực.
- `-v`: Kích hoạt chế độ chi tiết để hiển thị thông tin quá trình sao chép.

## Ví dụ thường gặp
1. Sao chép một file từ máy cục bộ đến máy từ xa:
   ```bash
   scp /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

2. Sao chép một file từ máy từ xa về máy cục bộ:
   ```bash
   scp username@remote_host:/path/to/remote/file /path/to/local/directory
   ```

3. Sao chép một thư mục từ máy cục bộ đến máy từ xa:
   ```bash
   scp -r /path/to/local/directory username@remote_host:/path/to/remote/directory
   ```

4. Sao chép một file qua cổng SSH khác:
   ```bash
   scp -P 2222 /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

## Mẹo
- Luôn kiểm tra kết nối SSH trước khi sử dụng `scp` để đảm bảo rằng bạn có quyền truy cập vào máy từ xa.
- Sử dụng tùy chọn `-v` để gỡ lỗi nếu bạn gặp vấn đề trong quá trình sao chép.
- Để tăng tốc độ sao chép, bạn có thể sử dụng tùy chọn `-C` để nén dữ liệu trong quá trình truyền tải.