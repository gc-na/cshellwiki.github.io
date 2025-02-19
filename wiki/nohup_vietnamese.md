# [Hệ điều hành] C Shell (csh) nohup: Chạy lệnh không bị ngắt kết nối

## Overview
Lệnh `nohup` trong C Shell (csh) cho phép bạn chạy một lệnh mà không bị ngắt kết nối khi bạn đăng xuất khỏi phiên làm việc. Điều này rất hữu ích khi bạn muốn thực hiện các tác vụ dài mà không cần phải giữ phiên mở.

## Usage
Cú pháp cơ bản của lệnh `nohup` như sau:
```
nohup [options] [arguments]
```

## Common Options
- `&`: Chạy lệnh ở chế độ nền.
- `-h`: Hiển thị thông tin trợ giúp về lệnh.
- `-v`: Hiển thị thông tin chi tiết về các lệnh đang chạy.

## Common Examples
1. Chạy một script shell trong nền mà không bị ngắt kết nối:
   ```csh
   nohup ./my_script.sh &
   ```

2. Chạy một lệnh dài và ghi lại đầu ra vào file `nohup.out`:
   ```csh
   nohup long_running_command > output.log &
   ```

3. Chạy lệnh `ping` liên tục mà không bị ngắt kết nối:
   ```csh
   nohup ping google.com &
   ```

## Tips
- Luôn kiểm tra file `nohup.out` để xem đầu ra của lệnh đã chạy.
- Sử dụng `&` để chạy lệnh trong nền, giúp bạn có thể tiếp tục sử dụng terminal cho các lệnh khác.
- Nếu bạn muốn dừng lệnh đang chạy, hãy sử dụng `kill` với PID của lệnh đó.