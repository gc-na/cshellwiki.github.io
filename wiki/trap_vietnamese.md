# [Linux] Bash trap cách sử dụng: Bắt và xử lý tín hiệu

## Overview
Lệnh `trap` trong Bash được sử dụng để bắt và xử lý các tín hiệu hoặc sự kiện trong quá trình thực thi của một script. Điều này cho phép người dùng thực hiện các hành động cụ thể khi một tín hiệu nhất định được nhận, như khi script bị dừng hoặc khi có lỗi xảy ra.

## Usage
Cú pháp cơ bản của lệnh `trap` như sau:

```bash
trap [options] [commands] [signals]
```

## Common Options
- `-l`: Liệt kê tất cả các tín hiệu có sẵn.
- `-p`: Hiển thị các lệnh trap hiện tại cho các tín hiệu.
- `SIGINT`: Tín hiệu ngắt (Ctrl+C).
- `SIGTERM`: Tín hiệu yêu cầu dừng.

## Common Examples

### Bắt tín hiệu SIGINT
Dưới đây là ví dụ về cách sử dụng `trap` để bắt tín hiệu ngắt:

```bash
trap 'echo "Script bị ngắt"; exit' SIGINT
while true; do
    echo "Đang chạy..."
    sleep 1
done
```

### Dọn dẹp tài nguyên trước khi thoát
Trong ví dụ này, chúng ta sẽ dọn dẹp tài nguyên khi script kết thúc:

```bash
trap 'echo "Đang dọn dẹp..."; rm -f temp_file.txt; exit' EXIT
touch temp_file.txt
echo "Script đang chạy..."
sleep 5
```

### Bắt nhiều tín hiệu
Bạn có thể bắt nhiều tín hiệu cùng một lúc:

```bash
trap 'echo "Đã nhận tín hiệu ngắt"; exit' SIGINT SIGTERM
while true; do
    echo "Đang chạy..."
    sleep 1
done
```

## Tips
- Sử dụng `trap` để đảm bảo rằng các tài nguyên được dọn dẹp đúng cách khi script kết thúc.
- Kiểm tra các tín hiệu có sẵn bằng cách sử dụng `trap -l` để biết tín hiệu nào có thể được bắt.
- Đặt lệnh `trap` ở đầu script để đảm bảo rằng nó luôn hoạt động từ đầu đến cuối.