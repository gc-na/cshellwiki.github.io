# [Linux] Bash else cú pháp: Câu lệnh điều kiện trong Bash

## Overview
Câu lệnh `else` trong Bash được sử dụng để thực hiện một khối lệnh khác nếu điều kiện trong câu lệnh `if` không được thỏa mãn. Đây là một phần quan trọng trong lập trình điều kiện, cho phép người dùng xử lý các tình huống khác nhau trong kịch bản của họ.

## Usage
Cú pháp cơ bản của câu lệnh `else` như sau:

```bash
if [ điều kiện ]; then
    # Lệnh thực hiện nếu điều kiện đúng
else
    # Lệnh thực hiện nếu điều kiện sai
fi
```

## Common Options
Câu lệnh `else` không có tùy chọn cụ thể nào, nhưng nó thường được sử dụng kết hợp với các câu lệnh `if` và `elif`. Dưới đây là một số điều kiện thường gặp:

- `[ -f file ]`: Kiểm tra xem file có tồn tại và là file thường không.
- `[ -d directory ]`: Kiểm tra xem thư mục có tồn tại không.
- `[ condition ]`: Kiểm tra bất kỳ điều kiện nào khác.

## Common Examples

### Ví dụ 1: Kiểm tra file tồn tại
```bash
if [ -f "file.txt" ]; then
    echo "File tồn tại."
else
    echo "File không tồn tại."
fi
```

### Ví dụ 2: Kiểm tra thư mục tồn tại
```bash
if [ -d "my_directory" ]; then
    echo "Thư mục tồn tại."
else
    echo "Thư mục không tồn tại."
fi
```

### Ví dụ 3: Sử dụng với biến
```bash
number=10
if [ $number -gt 5 ]; then
    echo "Số lớn hơn 5."
else
    echo "Số không lớn hơn 5."
fi
```

## Tips
- Luôn sử dụng dấu cách đúng giữa các dấu ngoặc vuông và điều kiện để tránh lỗi cú pháp.
- Bạn có thể kết hợp nhiều câu lệnh `elif` giữa `if` và `else` để xử lý nhiều điều kiện khác nhau.
- Đảm bảo rằng bạn kết thúc khối lệnh `if` với `fi` để xác định rõ ràng kết thúc của cấu trúc điều kiện.