# [Linux] Bash ss cách sử dụng: Xem thông tin kết nối mạng

## Overview
Lệnh `ss` được sử dụng để hiển thị thông tin về các kết nối mạng trên hệ thống. Nó là một công cụ mạnh mẽ giúp người dùng theo dõi và phân tích các kết nối TCP, UDP và các giao thức khác.

## Usage
Cú pháp cơ bản của lệnh `ss` như sau:
```bash
ss [options] [arguments]
```

## Common Options
- `-t`: Hiển thị các kết nối TCP.
- `-u`: Hiển thị các kết nối UDP.
- `-l`: Hiển thị các kết nối đang lắng nghe.
- `-p`: Hiển thị thông tin về tiến trình đang sử dụng kết nối.
- `-n`: Hiển thị địa chỉ và cổng mà không cần phân giải tên.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `ss`:

1. Hiển thị tất cả các kết nối TCP:
   ```bash
   ss -t
   ```

2. Hiển thị tất cả các kết nối UDP:
   ```bash
   ss -u
   ```

3. Hiển thị các kết nối đang lắng nghe:
   ```bash
   ss -l
   ```

4. Hiển thị thông tin về tiến trình sử dụng kết nối:
   ```bash
   ss -p
   ```

5. Hiển thị tất cả các kết nối với địa chỉ và cổng không phân giải tên:
   ```bash
   ss -n
   ```

## Tips
- Sử dụng kết hợp các tùy chọn để có được thông tin chi tiết hơn, chẳng hạn như `ss -tunlp` để xem tất cả các kết nối TCP và UDP đang lắng nghe cùng với thông tin tiến trình.
- Kiểm tra các kết nối mạng thường xuyên để phát hiện các vấn đề hoặc kết nối không mong muốn.
- Lệnh `ss` nhanh hơn và hiệu quả hơn so với lệnh `netstat`, vì vậy hãy cân nhắc sử dụng nó cho các tác vụ phân tích mạng.