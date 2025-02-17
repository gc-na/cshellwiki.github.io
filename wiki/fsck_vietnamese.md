# [Linux] Bash fsck Cách sử dụng: Kiểm tra và sửa lỗi hệ thống tập tin

## Tổng quan
Lệnh `fsck` (File System Consistency Check) được sử dụng để kiểm tra và sửa chữa các lỗi trong hệ thống tập tin trên các hệ điều hành Unix và Linux. Nó giúp đảm bảo rằng các tập tin và thư mục trên đĩa cứng hoạt động bình thường và không bị hỏng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `fsck` như sau:
```bash
fsck [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a` hoặc `--auto`: Tự động sửa chữa các lỗi mà không yêu cầu xác nhận từ người dùng.
- `-n` hoặc `--no`: Không sửa chữa, chỉ kiểm tra và báo cáo lỗi.
- `-y`: Tự động trả lời "yes" cho tất cả các câu hỏi, cho phép sửa chữa tất cả các lỗi.
- `-t`: Chỉ định loại hệ thống tập tin (ví dụ: ext4, xfs).
- `-f`: Buộc kiểm tra ngay cả khi hệ thống tập tin được đánh dấu là sạch.

## Ví dụ phổ biến
Dưới đây là một số ví dụ về cách sử dụng lệnh `fsck`:

1. Kiểm tra hệ thống tập tin trên phân vùng `/dev/sda1`:
   ```bash
   fsck /dev/sda1
   ```

2. Tự động sửa chữa các lỗi trên phân vùng `/dev/sda1`:
   ```bash
   fsck -a /dev/sda1
   ```

3. Kiểm tra mà không sửa chữa, chỉ báo cáo lỗi:
   ```bash
   fsck -n /dev/sda1
   ```

4. Tự động sửa chữa tất cả các lỗi mà không hỏi:
   ```bash
   fsck -y /dev/sda1
   ```

5. Kiểm tra hệ thống tập tin ext4 trên phân vùng `/dev/sdb1`:
   ```bash
   fsck -t ext4 /dev/sdb1
   ```

## Mẹo
- Luôn sao lưu dữ liệu quan trọng trước khi chạy `fsck`, đặc biệt khi sửa chữa lỗi.
- Nên chạy `fsck` khi hệ thống không hoạt động (ví dụ: từ môi trường khôi phục) để tránh xung đột với các tiến trình đang chạy.
- Kiểm tra định kỳ hệ thống tập tin để phát hiện sớm các lỗi tiềm ẩn và duy trì hiệu suất của hệ thống.