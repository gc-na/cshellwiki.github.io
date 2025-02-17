# [Linux] Bash umount Cách sử dụng: Gỡ bỏ hệ thống tệp

## Overview
Lệnh `umount` được sử dụng để gỡ bỏ (unmount) một hệ thống tệp đã được gắn kết (mounted) trong Linux. Khi một hệ thống tệp được gỡ bỏ, các tệp và thư mục trên đó sẽ không còn khả dụng cho người dùng hoặc các ứng dụng cho đến khi nó được gắn kết lại.

## Usage
Cú pháp cơ bản của lệnh `umount` như sau:
```
umount [options] [arguments]
```

## Common Options
- `-a`: Gỡ bỏ tất cả các hệ thống tệp được gắn kết trong `/etc/mtab`.
- `-f`: Gỡ bỏ một hệ thống tệp ngay cả khi nó đang được sử dụng.
- `-l`: Gỡ bỏ một hệ thống tệp một cách lười biếng (lazy), nghĩa là nó sẽ gỡ bỏ khi không còn được sử dụng.
- `-r`: Gỡ bỏ một hệ thống tệp và cố gắng khôi phục nếu có lỗi.

## Common Examples
Gỡ bỏ một hệ thống tệp cụ thể:
```bash
umount /mnt/mydrive
```

Gỡ bỏ tất cả các hệ thống tệp được gắn kết:
```bash
umount -a
```

Gỡ bỏ một hệ thống tệp ngay cả khi nó đang được sử dụng:
```bash
umount -f /mnt/mydrive
```

Gỡ bỏ một hệ thống tệp một cách lười biếng:
```bash
umount -l /mnt/mydrive
```

## Tips
- Trước khi gỡ bỏ một hệ thống tệp, hãy đảm bảo rằng không có ứng dụng nào đang sử dụng tệp trong đó để tránh mất dữ liệu.
- Sử dụng lệnh `df` để kiểm tra các hệ thống tệp đang được gắn kết trước khi thực hiện lệnh `umount`.
- Nếu gặp lỗi khi gỡ bỏ, hãy kiểm tra xem có tệp nào đang được mở hoặc có tiến trình nào đang sử dụng hệ thống tệp đó hay không.