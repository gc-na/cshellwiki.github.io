# [Linux] Bash dpkg Cách sử dụng: Quản lý gói phần mềm

## Tổng quan
Lệnh `dpkg` là một công cụ quản lý gói cho hệ điều hành Debian và các bản phân phối dựa trên Debian như Ubuntu. Nó cho phép người dùng cài đặt, gỡ bỏ và quản lý các gói phần mềm trên hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `dpkg` như sau:
```
dpkg [options] [arguments]
```

## Các tùy chọn phổ biến
- `-i`, `--install`: Cài đặt một gói phần mềm.
- `-r`, `--remove`: Gỡ bỏ một gói phần mềm.
- `-l`, `--list`: Liệt kê tất cả các gói đã cài đặt.
- `-s`, `--status`: Hiển thị thông tin trạng thái của một gói.
- `-c`, `--contents`: Hiển thị nội dung của một gói đã cài đặt.

## Ví dụ phổ biến
1. **Cài đặt một gói phần mềm:**
   ```bash
   sudo dpkg -i ten-goi.deb
   ```

2. **Gỡ bỏ một gói phần mềm:**
   ```bash
   sudo dpkg -r ten-goi
   ```

3. **Liệt kê tất cả các gói đã cài đặt:**
   ```bash
   dpkg -l
   ```

4. **Kiểm tra trạng thái của một gói:**
   ```bash
   dpkg -s ten-goi
   ```

5. **Xem nội dung của một gói:**
   ```bash
   dpkg -c ten-goi.deb
   ```

## Mẹo
- Luôn sử dụng `sudo` khi thực hiện các thao tác cài đặt hoặc gỡ bỏ gói để đảm bảo bạn có quyền truy cập cần thiết.
- Kiểm tra trạng thái của gói sau khi cài đặt để đảm bảo không có lỗi xảy ra.
- Sử dụng `dpkg --get-selections` để lưu danh sách các gói đã cài đặt, giúp bạn dễ dàng phục hồi hệ thống sau này.