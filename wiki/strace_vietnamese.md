# [Linux] Bash strace cách sử dụng: Theo dõi các cuộc gọi hệ thống

## Tổng quan
Lệnh `strace` là một công cụ mạnh mẽ trong Linux dùng để theo dõi và ghi lại các cuộc gọi hệ thống và tín hiệu mà một chương trình thực hiện. Nó rất hữu ích cho việc gỡ lỗi và phân tích hành vi của các ứng dụng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `strace` như sau:

```bash
strace [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-o <tên_tệp>`: Ghi đầu ra vào tệp thay vì hiển thị trên màn hình.
- `-e <biểu_thức>`: Chỉ theo dõi các cuộc gọi hệ thống cụ thể.
- `-p <pid>`: Theo dõi một tiến trình đang chạy với ID tiến trình (PID) đã cho.
- `-c`: Tóm tắt các cuộc gọi hệ thống và thời gian sử dụng.
- `-f`: Theo dõi các tiến trình con được tạo ra bởi tiến trình gốc.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng `strace`:

1. Theo dõi một lệnh đơn giản:
   ```bash
   strace ls
   ```

2. Ghi đầu ra vào tệp:
   ```bash
   strace -o output.txt ls
   ```

3. Theo dõi một tiến trình đang chạy:
   ```bash
   strace -p 1234
   ```

4. Chỉ theo dõi các cuộc gọi hệ thống liên quan đến tệp:
   ```bash
   strace -e trace=file ls
   ```

5. Tóm tắt các cuộc gọi hệ thống:
   ```bash
   strace -c ls
   ```

## Mẹo
- Sử dụng tùy chọn `-o` để lưu lại kết quả, giúp bạn dễ dàng phân tích sau này.
- Kết hợp `-e` với các tùy chọn khác để thu hẹp phạm vi theo dõi, giúp giảm lượng thông tin không cần thiết.
- Khi theo dõi một tiến trình đang chạy, hãy đảm bảo rằng bạn có quyền truy cập vào PID của tiến trình đó.
- Đọc tài liệu hướng dẫn bằng cách sử dụng `man strace` để tìm hiểu thêm về các tùy chọn và cách sử dụng.