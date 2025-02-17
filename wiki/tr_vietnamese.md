# [Linux] Bash tr <Sử dụng tương đương>: Chuyển đổi và thay thế ký tự

## Overview
Lệnh `tr` trong Bash được sử dụng để chuyển đổi hoặc thay thế các ký tự trong đầu vào. Nó thường được sử dụng để xử lý văn bản, như thay đổi chữ hoa thành chữ thường, hoặc loại bỏ các ký tự không mong muốn.

## Usage
Cú pháp cơ bản của lệnh `tr` như sau:
```bash
tr [options] [arguments]
```

## Common Options
- `-d`: Xóa các ký tự được chỉ định.
- `-s`: Rút gọn nhiều ký tự liên tiếp thành một ký tự.
- `-c`: Thay thế các ký tự không có trong danh sách.
- `-t`: Thay thế ký tự đầu vào với ký tự đầu ra.

## Common Examples
1. **Chuyển đổi chữ hoa thành chữ thường:**
   ```bash
   echo "HELLO WORLD" | tr 'A-Z' 'a-z'
   ```
   Kết quả: `hello world`

2. **Xóa các ký tự không phải chữ số:**
   ```bash
   echo "abc123def456" | tr -d 'a-z'
   ```
   Kết quả: `123456`

3. **Rút gọn nhiều khoảng trắng thành một khoảng trắng:**
   ```bash
   echo "This    is    a    test." | tr -s ' '
   ```
   Kết quả: `This is a test.`

4. **Thay thế ký tự:**
   ```bash
   echo "hello" | tr 'e' 'a'
   ```
   Kết quả: `hallo`

## Tips
- Sử dụng `tr` kết hợp với các lệnh khác như `grep` hoặc `sed` để xử lý văn bản hiệu quả hơn.
- Hãy cẩn thận với các ký tự đặc biệt; nếu bạn muốn thay thế hoặc xóa chúng, hãy đảm bảo bạn đã chỉ định đúng.
- Kiểm tra đầu ra của lệnh bằng cách sử dụng `echo` trước khi áp dụng `tr` để tránh mất dữ liệu không mong muốn.