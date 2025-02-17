# [Linux] Bash dstat Cách sử dụng: Theo dõi tài nguyên hệ thống theo thời gian thực

## Overview
Lệnh `dstat` là một công cụ mạnh mẽ dùng để theo dõi và hiển thị thông tin về tài nguyên hệ thống trong thời gian thực. Nó kết hợp nhiều thông tin từ các lệnh khác nhau như `vmstat`, `iostat`, `netstat`, và `ifstat`, giúp người dùng có cái nhìn tổng quan về hiệu suất hệ thống.

## Usage
Cú pháp cơ bản của lệnh `dstat` như sau:
```bash
dstat [options] [arguments]
```

## Common Options
- `-c`: Hiển thị thông tin về CPU.
- `-d`: Hiển thị thông tin về đĩa.
- `-n`: Hiển thị thông tin về mạng.
- `-r`: Hiển thị thông tin về bộ nhớ.
- `-t`: Hiển thị thời gian.
- `--help`: Hiển thị thông tin trợ giúp về lệnh.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `dstat`:

1. Hiển thị thông tin cơ bản về CPU và đĩa:
   ```bash
   dstat -c -d
   ```

2. Theo dõi thông tin về mạng và bộ nhớ:
   ```bash
   dstat -n -r
   ```

3. Hiển thị tất cả các thông tin cùng một lúc:
   ```bash
   dstat -cdrnt
   ```

4. Ghi thông tin vào file để phân tích sau:
   ```bash
   dstat -t --output my_dstat_output.csv
   ```

## Tips
- Sử dụng `dstat` với tùy chọn `--output` để lưu dữ liệu vào file, giúp bạn dễ dàng phân tích sau này.
- Kết hợp nhiều tùy chọn để có cái nhìn tổng quan hơn về tình trạng hệ thống.
- Thực hiện lệnh `dstat` với quyền root để có thể theo dõi tất cả các thông tin hệ thống mà không bị hạn chế.