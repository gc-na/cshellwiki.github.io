# [Hệ điều hành] C Shell (csh) mount: [gắn kết hệ thống tập tin]

## Tổng quan
Lệnh `mount` trong C Shell (csh) được sử dụng để gắn kết một hệ thống tập tin vào một điểm gắn kết trong hệ thống tệp của bạn. Điều này cho phép bạn truy cập các tệp và thư mục từ thiết bị lưu trữ bên ngoài như ổ đĩa cứng, USB, hoặc phân vùng khác.

## Cú pháp
Cú pháp cơ bản của lệnh `mount` như sau:
```
mount [options] [arguments]
```

## Tùy chọn phổ biến
- `-t type`: Chỉ định loại hệ thống tập tin (ví dụ: ext4, ntfs).
- `-o options`: Chỉ định các tùy chọn gắn kết bổ sung (ví dụ: ro cho chế độ chỉ đọc).
- `-a`: Gắn kết tất cả các hệ thống tập tin được chỉ định trong tệp `/etc/fstab`.
- `-r`: Gắn kết hệ thống tập tin ở chế độ chỉ đọc.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mount`:

1. Gắn kết một ổ đĩa USB vào thư mục `/mnt/usb`:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. Gắn kết một phân vùng NTFS ở chế độ chỉ đọc:
   ```bash
   mount -t ntfs -o ro /dev/sdc1 /mnt/ntfs
   ```

3. Gắn tất cả các hệ thống tập tin từ tệp `/etc/fstab`:
   ```bash
   mount -a
   ```

4. Gắn kết một phân vùng ext4 với tùy chọn gắn kết bổ sung:
   ```bash
   mount -t ext4 -o defaults,noatime /dev/sda1 /mnt/data
   ```

## Mẹo
- Luôn kiểm tra xem hệ thống tập tin đã được gắn kết hay chưa bằng lệnh `df -h` trước khi thực hiện các thao tác trên.
- Đảm bảo rằng bạn có quyền truy cập cần thiết để gắn kết các thiết bị lưu trữ.
- Sử dụng tùy chọn `-o loop` nếu bạn muốn gắn kết một tệp hình ảnh ISO như một hệ thống tập tin.
- Nhớ gỡ bỏ gắn kết hệ thống tập tin bằng lệnh `umount` sau khi sử dụng để tránh mất dữ liệu.