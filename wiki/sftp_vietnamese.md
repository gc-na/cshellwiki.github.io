# [Hệ điều hành] C Shell (csh) sftp: Chuyển tập tin an toàn

## Tổng quan
Lệnh `sftp` (SSH File Transfer Protocol) được sử dụng để truyền tải tập tin an toàn giữa máy khách và máy chủ qua giao thức SSH. Nó cho phép người dùng thực hiện các thao tác như tải lên, tải xuống và quản lý tập tin trên máy chủ từ xa.

## Cú pháp
Cú pháp cơ bản của lệnh `sftp` như sau:
```
sftp [options] [user@]host
```

## Các tùy chọn thông dụng
- `-b <file>`: Chạy lệnh từ một tệp lệnh.
- `-C`: Bật nén dữ liệu.
- `-i <file>`: Chỉ định tệp khóa riêng để xác thực.
- `-o <option>`: Chỉ định tùy chọn cho phiên kết nối SSH.
- `-P <port>`: Chỉ định cổng kết nối.

## Ví dụ thông dụng
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `sftp`:

1. Kết nối đến máy chủ SFTP:
   ```bash
   sftp user@hostname
   ```

2. Tải xuống một tệp từ máy chủ:
   ```bash
   get remote_file.txt
   ```

3. Tải lên một tệp đến máy chủ:
   ```bash
   put local_file.txt
   ```

4. Liệt kê các tệp trong thư mục hiện tại trên máy chủ:
   ```bash
   ls
   ```

5. Tạo một thư mục mới trên máy chủ:
   ```bash
   mkdir new_directory
   ```

## Mẹo
- Luôn kiểm tra kết nối mạng trước khi sử dụng `sftp` để đảm bảo truyền tải thành công.
- Sử dụng tùy chọn `-C` để tăng tốc độ truyền tải bằng cách nén dữ liệu.
- Để tự động hóa các tác vụ, bạn có thể sử dụng tệp lệnh với tùy chọn `-b`.
- Đảm bảo rằng bạn có quyền truy cập cần thiết trên máy chủ để thực hiện các thao tác như tải lên hoặc xóa tệp.