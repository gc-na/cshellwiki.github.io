# [Linux] Bash mount sử dụng: Gắn kết hệ thống tệp

## Overview
Lệnh `mount` trong Bash được sử dụng để gắn kết một hệ thống tệp vào một điểm gắn kết trong cây thư mục của hệ thống. Điều này cho phép người dùng truy cập vào các tệp và thư mục trên thiết bị lưu trữ bên ngoài hoặc phân vùng khác.

## Usage
Cú pháp cơ bản của lệnh `mount` như sau:
```
mount [options] [arguments]
```

## Common Options
- `-t <type>`: Chỉ định loại hệ thống tệp (ví dụ: ext4, ntfs).
- `-o <options>`: Chỉ định các tùy chọn gắn kết (ví dụ: ro cho chế độ chỉ đọc).
- `-a`: Gắn tất cả các hệ thống tệp được chỉ định trong tệp fstab.
- `-r`: Gắn hệ thống tệp ở chế độ chỉ đọc.

## Common Examples
1. Gắn một phân vùng ext4:
   ```bash
   mount -t ext4 /dev/sda1 /mnt/mydrive
   ```

2. Gắn một phân vùng NTFS với chế độ chỉ đọc:
   ```bash
   mount -t ntfs -o ro /dev/sdb1 /mnt/ntfsdrive
   ```

3. Gắn tất cả các hệ thống tệp từ fstab:
   ```bash
   mount -a
   ```

4. Gắn một phân vùng với các tùy chọn bổ sung:
   ```bash
   mount -t ext4 -o rw,noexec /dev/sdc1 /mnt/usbdrive
   ```

## Tips
- Luôn kiểm tra điểm gắn kết trước khi gắn để đảm bảo rằng nó không bị sử dụng.
- Sử dụng lệnh `umount` để gỡ bỏ gắn kết một hệ thống tệp trước khi rút thiết bị.
- Kiểm tra tệp `/etc/fstab` để quản lý các hệ thống tệp tự động gắn kết khi khởi động.