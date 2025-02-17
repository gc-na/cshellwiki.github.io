# [Bash] Bash while sử dụng: Lặp lại một khối lệnh

## Overview
Lệnh `while` trong Bash cho phép bạn lặp lại một khối lệnh cho đến khi điều kiện được chỉ định trở thành sai. Điều này rất hữu ích khi bạn cần thực hiện một tác vụ nhiều lần cho đến khi một điều kiện cụ thể không còn đúng nữa.

## Usage
Cú pháp cơ bản của lệnh `while` như sau:

```bash
while [ điều kiện ]
do
    # lệnh cần thực hiện
done
```

## Common Options
- Không có tùy chọn cụ thể cho lệnh `while`, nhưng bạn có thể sử dụng các biểu thức điều kiện khác nhau để kiểm tra trạng thái.

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

### Ví dụ 2: Đọc từ tệp cho đến khi hết
```bash
while IFS= read -r line
do
    echo "$line"
done < file.txt
```

### Ví dụ 3: Lặp lại cho đến khi người dùng nhập 'exit'
```bash
input=""
while [ "$input" != "exit" ]
do
    read -p "Nhập một lệnh (hoặc 'exit' để thoát): " input
    echo "Bạn đã nhập: $input"
done
```

## Tips
- Hãy chắc chắn rằng điều kiện trong lệnh `while` sẽ trở thành sai tại một thời điểm nào đó để tránh vòng lặp vô hạn.
- Sử dụng `break` để thoát khỏi vòng lặp nếu cần thiết.
- Sử dụng `continue` để bỏ qua phần còn lại của vòng lặp và bắt đầu lại từ đầu.