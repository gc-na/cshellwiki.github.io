# [Linux] Bash netstat Cách sử dụng: Kiểm tra kết nối mạng

## Overview
Lệnh `netstat` là một công cụ mạnh mẽ trong Bash được sử dụng để hiển thị thông tin về các kết nối mạng, bảng định tuyến, và các giao thức mạng đang hoạt động trên hệ thống. Nó giúp người dùng theo dõi và phân tích tình trạng mạng của máy tính.

## Usage
Cú pháp cơ bản của lệnh `netstat` như sau:

```bash
netstat [options] [arguments]
```

## Common Options
Dưới đây là một số tùy chọn phổ biến của lệnh `netstat`:

- `-a`: Hiển thị tất cả các kết nối và cổng đang lắng nghe.
- `-t`: Hiển thị các kết nối TCP.
- `-u`: Hiển thị các kết nối UDP.
- `-n`: Hiển thị địa chỉ và số cổng dưới dạng số thay vì tên.
- `-l`: Hiển thị các cổng đang lắng nghe.
- `-p`: Hiển thị PID và tên của chương trình đang sử dụng kết nối.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `netstat`:

1. Hiển thị tất cả các kết nối và cổng đang lắng nghe:
   ```bash
   netstat -a
   ```

2. Hiển thị các kết nối TCP:
   ```bash
   netstat -t
   ```

3. Hiển thị các kết nối UDP:
   ```bash
   netstat -u
   ```

4. Hiển thị địa chỉ và số cổng dưới dạng số:
   ```bash
   netstat -n
   ```

5. Hiển thị các cổng đang lắng nghe:
   ```bash
   netstat -l
   ```

6. Hiển thị PID và tên của chương trình đang sử dụng kết nối:
   ```bash
   netstat -p
   ```

## Tips
- Sử dụng `netstat -tuln` để nhanh chóng xem các cổng TCP và UDP đang lắng nghe mà không cần tên.
- Kết hợp `grep` với `netstat` để tìm kiếm thông tin cụ thể, ví dụ: `netstat -tuln | grep 80` để tìm các kết nối trên cổng 80.
- Thường xuyên kiểm tra kết nối mạng của bạn để phát hiện các hoạt động bất thường hoặc không mong muốn.