# [Hệ điều hành] C Shell (csh) hostname: Lấy tên máy chủ

## Overview
Lệnh `hostname` trong C Shell (csh) được sử dụng để hiển thị hoặc thiết lập tên máy chủ của hệ thống. Tên máy chủ là một phần quan trọng trong việc xác định và quản lý các máy tính trong một mạng.

## Usage
Cú pháp cơ bản của lệnh `hostname` như sau:

```csh
hostname [options] [arguments]
```

## Common Options
- `-s`: Hiển thị tên máy chủ ngắn (hostname).
- `-f`: Hiển thị tên máy chủ đầy đủ (fully qualified domain name - FQDN).
- `-i`: Hiển thị địa chỉ IP của máy chủ.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `hostname`:

1. Hiển thị tên máy chủ hiện tại:
   ```csh
   hostname
   ```

2. Hiển thị tên máy chủ ngắn:
   ```csh
   hostname -s
   ```

3. Hiển thị tên máy chủ đầy đủ:
   ```csh
   hostname -f
   ```

4. Hiển thị địa chỉ IP của máy chủ:
   ```csh
   hostname -i
   ```

5. Thiết lập tên máy chủ mới:
   ```csh
   hostname new-hostname
   ```

## Tips
- Để thay đổi tên máy chủ, bạn cần quyền quản trị (root).
- Sau khi thay đổi tên máy chủ, bạn có thể cần khởi động lại hệ thống để thay đổi có hiệu lực.
- Kiểm tra tên máy chủ thường xuyên có thể giúp bạn xác định vị trí của máy trong mạng một cách dễ dàng hơn.