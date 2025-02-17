# [Linux] Bash ulimit: Quản lý giới hạn tài nguyên hệ thống

## Overview
Lệnh `ulimit` trong Bash được sử dụng để quản lý các giới hạn tài nguyên mà một phiên làm việc hoặc một tiến trình có thể sử dụng. Điều này bao gồm bộ nhớ, số lượng tệp mở, thời gian CPU, và nhiều tài nguyên khác. Việc thiết lập các giới hạn này giúp bảo vệ hệ thống khỏi việc sử dụng quá mức tài nguyên, có thể dẫn đến hiệu suất kém hoặc treo hệ thống.

## Usage
Cú pháp cơ bản của lệnh `ulimit` như sau:
```
ulimit [options] [arguments]
```

## Common Options
- `-a`: Hiển thị tất cả các giới hạn hiện tại.
- `-c`: Đặt hoặc hiển thị kích thước tệp core dump.
- `-d`: Đặt hoặc hiển thị kích thước bộ nhớ dữ liệu.
- `-f`: Đặt hoặc hiển thị kích thước tệp tối đa có thể tạo.
- `-l`: Đặt hoặc hiển thị kích thước bộ nhớ có thể khóa.
- `-n`: Đặt hoặc hiển thị số lượng tệp mở tối đa.
- `-s`: Đặt hoặc hiển thị kích thước ngăn xếp.
- `-t`: Đặt hoặc hiển thị thời gian CPU tối đa cho một tiến trình.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `ulimit`:

1. Hiển thị tất cả các giới hạn tài nguyên hiện tại:
   ```bash
   ulimit -a
   ```

2. Đặt giới hạn số lượng tệp mở tối đa là 1024:
   ```bash
   ulimit -n 1024
   ```

3. Đặt giới hạn kích thước tệp core dump là 0 (không cho phép tạo tệp core dump):
   ```bash
   ulimit -c 0
   ```

4. Kiểm tra giới hạn kích thước ngăn xếp hiện tại:
   ```bash
   ulimit -s
   ```

5. Đặt giới hạn thời gian CPU tối đa là 60 giây:
   ```bash
   ulimit -t 60
   ```

## Tips
- Nên kiểm tra các giới hạn hiện tại trước khi thay đổi để tránh gây ra sự cố cho các tiến trình đang chạy.
- Sử dụng lệnh `ulimit` trong các script để đảm bảo rằng các giới hạn tài nguyên được thiết lập đúng cách cho các tiến trình mà bạn khởi chạy.
- Lưu ý rằng các thay đổi giới hạn tài nguyên chỉ có hiệu lực cho phiên làm việc hiện tại và sẽ không ảnh hưởng đến các phiên khác hoặc sau khi đăng xuất.