# [Linux] Bash endif <Sử dụng tương đương>: Kết thúc một khối lệnh điều kiện

## Overview
Lệnh `endif` trong Bash được sử dụng để đánh dấu kết thúc của một khối lệnh điều kiện, thường là sau một câu lệnh `if`. Nó không phải là một lệnh độc lập mà là một phần của cấu trúc điều kiện trong script Bash.

## Usage
Cú pháp cơ bản của lệnh `endif` như sau:
```bash
endif
```

## Common Options
Lệnh `endif` không có tùy chọn nào vì nó chỉ đơn giản là một từ khóa để kết thúc khối lệnh điều kiện.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng `endif` trong Bash:

### Ví dụ 1: Cấu trúc điều kiện đơn giản
```bash
if [ "$a" -lt 100 ]; then
    echo "a nhỏ hơn 100"
endif
```

### Ví dụ 2: Sử dụng với lệnh `else`
```bash
if [ "$a" -lt 100 ]; then
    echo "a nhỏ hơn 100"
else
    echo "a lớn hơn hoặc bằng 100"
endif
```

### Ví dụ 3: Kết hợp với lệnh `elif`
```bash
if [ "$a" -lt 100 ]; then
    echo "a nhỏ hơn 100"
elif [ "$a" -eq 100 ]; then
    echo "a bằng 100"
else
    echo "a lớn hơn 100"
endif
```

## Tips
- Hãy chắc chắn rằng bạn sử dụng `endif` đúng cách để kết thúc các khối lệnh điều kiện, điều này giúp mã của bạn dễ đọc và dễ bảo trì hơn.
- Trong Bash, bạn cũng có thể sử dụng dấu ngoặc nhọn `{}` hoặc từ khóa `fi` để kết thúc khối lệnh điều kiện, vì vậy hãy chọn cách phù hợp với phong cách lập trình của bạn.