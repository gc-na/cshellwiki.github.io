# [Linux] Bash if: Kiểm tra điều kiện trong Bash

## Overview
Lệnh `if` trong Bash được sử dụng để kiểm tra các điều kiện và thực hiện các lệnh khác nhau dựa trên kết quả của các điều kiện đó. Đây là một phần quan trọng trong lập trình shell, cho phép bạn kiểm soát luồng thực thi của các lệnh.

## Usage
Cú pháp cơ bản của lệnh `if` như sau:

```bash
if [ điều kiện ]; then
    # lệnh thực hiện nếu điều kiện đúng
else
    # lệnh thực hiện nếu điều kiện sai
fi
```

## Common Options
- `-e`: Kiểm tra xem tệp có tồn tại hay không.
- `-d`: Kiểm tra xem tệp có phải là thư mục hay không.
- `-f`: Kiểm tra xem tệp có phải là tệp thường hay không.
- `-z`: Kiểm tra xem chuỗi có rỗng hay không.
- `-n`: Kiểm tra xem chuỗi có không rỗng hay không.

## Common Examples

### Ví dụ 1: Kiểm tra tệp tồn tại
```bash
if [ -e "file.txt" ]; then
    echo "Tệp tồn tại."
else
    echo "Tệp không tồn tại."
fi
```

### Ví dụ 2: Kiểm tra thư mục
```bash
if [ -d "my_directory" ]; then
    echo "Đây là một thư mục."
else
    echo "Đây không phải là một thư mục."
fi
```

### Ví dụ 3: Kiểm tra chuỗi
```bash
my_string="Hello"
if [ -n "$my_string" ]; then
    echo "Chuỗi không rỗng."
else
    echo "Chuỗi rỗng."
fi
```

### Ví dụ 4: So sánh số
```bash
num=10
if [ $num -gt 5 ]; then
    echo "Số lớn hơn 5."
else
    echo "Số không lớn hơn 5."
fi
```

## Tips
- Luôn sử dụng dấu cách đúng cách giữa các dấu ngoặc vuông và điều kiện.
- Sử dụng `elif` để kiểm tra nhiều điều kiện khác nhau trong cùng một lệnh `if`.
- Đặt các lệnh trong khối `then` và `else` trên các dòng mới để dễ đọc hơn.