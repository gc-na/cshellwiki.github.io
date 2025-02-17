# [Bash] Bash host sử dụng: Truy vấn thông tin DNS

## Overview
Lệnh `host` được sử dụng để truy vấn thông tin DNS (Domain Name System). Nó cho phép người dùng tìm kiếm địa chỉ IP cho tên miền hoặc ngược lại, tìm kiếm tên miền cho một địa chỉ IP cụ thể.

## Usage
Cú pháp cơ bản của lệnh `host` như sau:
```bash
host [options] [arguments]
```

## Common Options
- `-a`: Truy vấn tất cả các loại bản ghi DNS cho tên miền.
- `-t [type]`: Chỉ định loại bản ghi DNS cần truy vấn, ví dụ như A, MX, hoặc TXT.
- `-v`: Bật chế độ chi tiết, hiển thị thông tin bổ sung về truy vấn.
- `-W [seconds]`: Đặt thời gian chờ cho truy vấn DNS.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `host`:

1. **Tìm địa chỉ IP cho một tên miền:**
   ```bash
   host example.com
   ```

2. **Tìm tên miền cho một địa chỉ IP:**
   ```bash
   host 93.184.216.34
   ```

3. **Truy vấn tất cả các bản ghi DNS cho một tên miền:**
   ```bash
   host -a example.com
   ```

4. **Truy vấn loại bản ghi MX cho một tên miền:**
   ```bash
   host -t MX example.com
   ```

5. **Sử dụng chế độ chi tiết:**
   ```bash
   host -v example.com
   ```

## Tips
- Sử dụng tùy chọn `-t` để chỉ định loại bản ghi bạn cần, giúp tiết kiệm thời gian và tài nguyên.
- Khi làm việc với nhiều tên miền, bạn có thể sử dụng một tập tin chứa danh sách tên miền và lặp qua chúng với một vòng lặp trong Bash.
- Kiểm tra kết nối mạng của bạn nếu lệnh `host` không trả về kết quả như mong đợi, vì nó phụ thuộc vào khả năng truy cập DNS.