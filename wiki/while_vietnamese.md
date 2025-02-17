# [Linux] Bash while: Lặp lại một khối lệnh

## Overview
Lệnh `while` trong Bash được sử dụng để thực hiện lặp lại một khối lệnh cho đến khi điều kiện xác định trở thành sai. Điều này cho phép bạn tự động hóa các tác vụ lặp đi lặp lại mà không cần phải viết mã lặp lại nhiều lần.

## Usage
Cú pháp cơ bản của lệnh `while` như sau:

```bash
while [ điều kiện ]
do
    # các lệnh cần thực hiện
done
```

## Common Options
- `-n`: Kiểm tra xem chuỗi có độ dài khác không.
- `-z`: Kiểm tra xem chuỗi có độ dài bằng không không.

## Common Examples

### Ví dụ 1: Đếm từ 1 đến 5
```bash
count=1
while [ $count -le 5 ]
do
    echo "Số: $count"
    ((count++))
done
```

### Ví dụ 2: Đọc từ một tệp cho đến khi hết
```bash
while IFS= read -r line
do
    echo "Dòng: $line"
done < tệp.txt
```

### Ví dụ 3: Lặp lại cho đến khi người dùng nhập "exit"
```bash
input=""
while [ "$input" != "exit" ]
do
    read -p "Nhập lệnh (hoặc 'exit' để thoát): " input
    echo "Bạn đã nhập: $input"
done
```

## Tips
- Đảm bảo rằng điều kiện trong vòng lặp `while` sẽ trở thành sai để tránh vòng lặp vô hạn.
- Sử dụng `break` để thoát khỏi vòng lặp khi cần thiết.
- Sử dụng `continue` để bỏ qua phần còn lại của vòng lặp và quay lại điều kiện kiểm tra.