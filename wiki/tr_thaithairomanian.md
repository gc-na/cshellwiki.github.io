# [Bash] tr <Sử dụng tương đương>: Chuyển đổi hoặc xóa ký tự trong văn bản

## Overview
Lệnh `tr` trong Bash được sử dụng để chuyển đổi hoặc xóa các ký tự trong văn bản. Nó rất hữu ích trong việc xử lý văn bản, cho phép người dùng thay thế một tập hợp các ký tự bằng một tập hợp khác hoặc loại bỏ các ký tự không mong muốn.

## Usage
Cú pháp cơ bản của lệnh `tr` như sau:
```bash
tr [options] [arguments]
```

## Common Options
- `-d`: Xóa các ký tự được chỉ định.
- `-s`: Rút gọn các ký tự liên tiếp thành một ký tự duy nhất.
- `-c`: Chuyển đổi các ký tự không được chỉ định.
- `-t`: Thay thế các ký tự trong tập hợp đầu vào với các ký tự trong tập hợp đầu ra.

## Common Examples
### Thay thế ký tự
Thay thế tất cả các ký tự 'a' bằng 'b':
```bash
echo "banana" | tr 'a' 'b'
```

### Xóa ký tự
Xóa tất cả các ký tự 'a':
```bash
echo "banana" | tr -d 'a'
```

### Rút gọn ký tự
Rút gọn các khoảng trắng liên tiếp thành một khoảng trắng đơn:
```bash
echo "Hello    World" | tr -s ' '
```

### Chuyển đổi chữ hoa thành chữ thường
Chuyển đổi tất cả các ký tự chữ hoa thành chữ thường:
```bash
echo "HELLO" | tr 'A-Z' 'a-z'
```

## Tips
- Sử dụng `tr` trong các ống lệnh để xử lý văn bản một cách hiệu quả.
- Kết hợp `tr` với các lệnh khác như `grep` hoặc `sed` để tạo ra các quy trình xử lý văn bản phức tạp hơn.
- Hãy cẩn thận với các ký tự đặc biệt, vì chúng có thể có ý nghĩa đặc biệt trong Bash.