# [Linux] Bash modprobe cách sử dụng: Quản lý mô-đun kernel

## Tổng quan
Lệnh `modprobe` được sử dụng để tải hoặc gỡ bỏ các mô-đun kernel trong hệ điều hành Linux. Nó giúp quản lý các mô-đun cần thiết cho phần cứng hoặc các chức năng hệ thống khác.

## Cách sử dụng
Cú pháp cơ bản của lệnh `modprobe` như sau:
```
modprobe [options] [arguments]
```

## Các tùy chọn phổ biến
- `-r`, `--remove`: Gỡ bỏ mô-đun.
- `-n`, `--dry-run`: Thực hiện một thử nghiệm mà không thay đổi gì.
- `-v`, `--verbose`: Hiển thị thông tin chi tiết về quá trình tải hoặc gỡ bỏ mô-đun.
- `--show`: Hiển thị các mô-đun mà lệnh sẽ tải mà không thực hiện.

## Ví dụ phổ biến
1. Tải một mô-đun:
   ```bash
   modprobe nvidia
   ```

2. Gỡ bỏ một mô-đun:
   ```bash
   modprobe -r nvidia
   ```

3. Thực hiện thử nghiệm tải mô-đun mà không thay đổi gì:
   ```bash
   modprobe -n nvidia
   ```

4. Hiển thị thông tin chi tiết khi tải mô-đun:
   ```bash
   modprobe -v nvidia
   ```

## Mẹo
- Luôn kiểm tra xem mô-đun đã được tải hay chưa bằng lệnh `lsmod` trước khi sử dụng `modprobe`.
- Sử dụng tùy chọn `-v` để theo dõi quá trình tải mô-đun, giúp bạn dễ dàng phát hiện lỗi.
- Đảm bảo rằng bạn có quyền root hoặc sử dụng `sudo` khi thực hiện các thao tác với `modprobe`.