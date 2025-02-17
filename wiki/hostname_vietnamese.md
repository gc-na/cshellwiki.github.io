# [Linux] Bash hostname cách sử dụng: [hiển thị tên máy tính]

## Tổng quan
Lệnh `hostname` trong Bash được sử dụng để hiển thị hoặc thay đổi tên máy tính của hệ thống. Tên máy tính là một phần quan trọng trong việc xác định và quản lý các thiết bị trong mạng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `hostname` như sau:

```bash
hostname [tùy chọn] [tham số]
```

## Tùy chọn phổ biến
- `-s`: Hiển thị tên máy tính ngắn.
- `-f`: Hiển thị tên máy tính đầy đủ (FQDN).
- `-i`: Hiển thị địa chỉ IP của máy tính.
- `-d`: Hiển thị tên miền của máy tính.

## Ví dụ phổ biến
1. Hiển thị tên máy tính hiện tại:
   ```bash
   hostname
   ```

2. Hiển thị tên máy tính ngắn:
   ```bash
   hostname -s
   ```

3. Hiển thị tên máy tính đầy đủ:
   ```bash
   hostname -f
   ```

4. Hiển thị địa chỉ IP của máy tính:
   ```bash
   hostname -i
   ```

5. Đặt tên máy tính mới:
   ```bash
   sudo hostname new-name
   ```

## Mẹo
- Khi thay đổi tên máy tính, hãy đảm bảo rằng tên mới không trùng với tên của bất kỳ thiết bị nào khác trong mạng.
- Sau khi thay đổi tên máy tính, bạn có thể cần khởi động lại hệ thống hoặc dịch vụ mạng để thay đổi có hiệu lực.
- Sử dụng lệnh `hostnamectl` trên các hệ thống sử dụng systemd để quản lý tên máy tính một cách dễ dàng hơn.