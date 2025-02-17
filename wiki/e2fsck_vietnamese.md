# [Linux] Bash e2fsck Cách sử dụng: Kiểm tra và sửa lỗi hệ thống tệp Ext2/Ext3/Ext4

## Tổng quan
Lệnh `e2fsck` được sử dụng để kiểm tra và sửa chữa các lỗi trong hệ thống tệp Ext2, Ext3 và Ext4. Đây là một công cụ quan trọng giúp duy trì tính toàn vẹn của dữ liệu trên các phân vùng sử dụng các hệ thống tệp này.

## Cách sử dụng
Cú pháp cơ bản của lệnh `e2fsck` như sau:
```
e2fsck [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-p`: Tự động sửa chữa các lỗi mà không yêu cầu xác nhận.
- `-f`: Kiểm tra ngay cả khi hệ thống tệp được đánh dấu là sạch.
- `-n`: Không sửa chữa, chỉ kiểm tra và hiển thị các lỗi.
- `-y`: Tự động trả lời "có" cho tất cả các câu hỏi sửa chữa.
- `-c`: Kiểm tra các block xấu trên phân vùng.

## Ví dụ phổ biến
Dưới đây là một số ví dụ về cách sử dụng lệnh `e2fsck`:

1. Kiểm tra một phân vùng cụ thể:
   ```bash
   e2fsck /dev/sda1
   ```

2. Tự động sửa chữa các lỗi mà không cần xác nhận:
   ```bash
   e2fsck -p /dev/sda1
   ```

3. Kiểm tra và sửa lỗi, tự động trả lời "có" cho tất cả các câu hỏi:
   ```bash
   e2fsck -y /dev/sda1
   ```

4. Kiểm tra block xấu trên phân vùng:
   ```bash
   e2fsck -c /dev/sda1
   ```

## Mẹo
- Luôn sao lưu dữ liệu quan trọng trước khi chạy `e2fsck`, đặc biệt là khi sửa chữa lỗi.
- Nên chạy lệnh này khi phân vùng không được gắn kết (unmounted) để tránh hư hại dữ liệu.
- Sử dụng tùy chọn `-n` để kiểm tra trước khi thực hiện sửa chữa thực tế, giúp bạn hiểu rõ hơn về các lỗi có thể xảy ra.