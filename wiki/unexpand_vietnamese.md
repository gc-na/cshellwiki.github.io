# [Linux] Bash unexpand Cách sử dụng: Chuyển đổi khoảng trắng thành tab

## Overview
Lệnh `unexpand` trong Bash được sử dụng để chuyển đổi các khoảng trắng (spaces) trong một tệp thành các ký tự tab (tabs). Điều này hữu ích khi bạn muốn giảm kích thước của tệp hoặc chuẩn hóa định dạng văn bản.

## Usage
Cú pháp cơ bản của lệnh `unexpand` như sau:
```bash
unexpand [options] [arguments]
```

## Common Options
- `-a`, `--all`: Chuyển đổi tất cả các khoảng trắng thành tab.
- `-t N`, `--tabs=N`: Đặt chiều rộng tab là N ký tự. Mặc định là 8 ký tự.
- `-h`, `--help`: Hiển thị thông tin trợ giúp về lệnh.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `unexpand`:

1. Chuyển đổi khoảng trắng thành tab trong một tệp:
   ```bash
   unexpand input.txt > output.txt
   ```

2. Chuyển đổi tất cả khoảng trắng thành tab:
   ```bash
   unexpand -a input.txt > output.txt
   ```

3. Đặt chiều rộng tab là 4 ký tự:
   ```bash
   unexpand -t 4 input.txt > output.txt
   ```

4. Hiển thị thông tin trợ giúp:
   ```bash
   unexpand --help
   ```

## Tips
- Sử dụng `unexpand` cùng với `expand` để chuyển đổi qua lại giữa khoảng trắng và tab một cách dễ dàng.
- Kiểm tra định dạng tệp đầu vào trước khi sử dụng `unexpand` để đảm bảo rằng các khoảng trắng được xử lý đúng cách.
- Bạn có thể kết hợp `unexpand` với các lệnh khác trong Bash để xử lý tệp theo cách tự động hóa.