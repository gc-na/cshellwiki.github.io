# [Linux] Bash mount cách sử dụng: Gắn kết hệ thống tập tin

## Tổng quan
Lệnh `mount` trong Bash được sử dụng để gắn kết một hệ thống tập tin vào một điểm trong hệ thống tập tin hiện tại. Điều này cho phép người dùng truy cập vào các tập tin và thư mục trên thiết bị lưu trữ bên ngoài hoặc phân vùng khác.

## Cách sử dụng
Cú pháp cơ bản của lệnh `mount` như sau:
```bash
mount [options] [arguments]
```

## Tùy chọn phổ biến
- `-t type`: Chỉ định loại hệ thống tập tin (ví dụ: ext4, ntfs).
- `-o options`: Chỉ định các tùy chọn gắn kết (ví dụ: ro cho chỉ đọc, rw cho đọc và ghi).
- `-a`: Gắn kết tất cả các hệ thống tập tin được liệt kê trong file `/etc/fstab`.
- `-r`: Gắn kết hệ thống tập tin ở chế độ chỉ đọc.

## Ví dụ phổ biến
1. Gắn kết một phân vùng ext4:
   ```bash
   mount -t ext4 /dev/sdb1 /mnt/mydrive
   ```

2. Gắn kết một ổ đĩa USB với chế độ chỉ đọc:
   ```bash
   mount -o ro /dev/sdc1 /mnt/usb
   ```

3. Gắn kết tất cả các hệ thống tập tin từ file fstab:
   ```bash
   mount -a
   ```

4. Gắn kết một hệ thống tập tin NTFS:
   ```bash
   mount -t ntfs-3g /dev/sdd1 /mnt/ntfsdrive
   ```

## Mẹo
- Luôn kiểm tra trạng thái của các phân vùng trước khi gắn kết bằng lệnh `lsblk` để tránh lỗi.
- Sử dụng tùy chọn `-o noexec` nếu bạn không muốn cho phép thực thi các tập tin trên hệ thống tập tin được gắn kết.
- Để gỡ bỏ một hệ thống tập tin đã gắn kết, sử dụng lệnh `umount` theo sau là điểm gắn kết hoặc thiết bị.