# [Linux] Bash trap sử dụng: Quản lý tín hiệu trong Bash

## Overview
Lệnh `trap` trong Bash được sử dụng để quản lý các tín hiệu và sự kiện trong quá trình thực thi của một script. Nó cho phép bạn xác định các hành động cụ thể sẽ được thực hiện khi nhận được một tín hiệu nhất định, giúp bạn kiểm soát cách mà script phản ứng với các tình huống không mong muốn.

## Usage
Cú pháp cơ bản của lệnh `trap` như sau:

```bash
trap [options] [arguments]
```

## Common Options
- `SIGINT`: Tín hiệu ngắt (Ctrl+C).
- `SIGTERM`: Tín hiệu yêu cầu dừng chương trình.
- `EXIT`: Hành động sẽ được thực hiện khi script kết thúc.
- `ERR`: Hành động sẽ được thực hiện khi có lỗi xảy ra trong script.

## Common Examples

### Ví dụ 1: Ngăn chặn ngắt bằng Ctrl+C
```bash
trap 'echo "Script bị ngắt"; exit' SIGINT
while true; do
    echo "Đang chạy..."
    sleep 1
done
```
Trong ví dụ này, khi người dùng nhấn Ctrl+C, thông báo "Script bị ngắt" sẽ được in ra và script sẽ dừng lại.

### Ví dụ 2: Thực hiện hành động khi script kết thúc
```bash
trap 'echo "Script đã kết thúc."' EXIT
echo "Chạy script..."
sleep 3
```
Khi script kết thúc, thông báo "Script đã kết thúc." sẽ được in ra.

### Ví dụ 3: Xử lý lỗi
```bash
trap 'echo "Có lỗi xảy ra!"' ERR
false  # Lệnh này sẽ tạo ra lỗi
```
Khi lệnh `false` gây ra lỗi, thông báo "Có lỗi xảy ra!" sẽ được in ra.

## Tips
- Sử dụng `trap` để dọn dẹp tài nguyên như tệp tin tạm thời khi script kết thúc.
- Đảm bảo rằng các hành động trong `trap` không mất quá nhiều thời gian để tránh làm chậm quá trình kết thúc của script.
- Kiểm tra các tín hiệu mà script có thể nhận được để xác định cách xử lý phù hợp.