# [Linux] Bash getopts Cách sử dụng: Quản lý tham số dòng lệnh

## Tổng quan
Lệnh `getopts` trong Bash được sử dụng để phân tích và xử lý các tham số dòng lệnh. Nó giúp lập trình viên dễ dàng quản lý các tùy chọn và đối số được truyền vào script, cho phép tạo ra các script linh hoạt và dễ sử dụng hơn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `getopts` như sau:
```bash
getopts [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`: Chỉ định một tham số tùy chọn.
- `-b`: Chỉ định một tham số bắt buộc.
- `-c`: Chạy một hành động cụ thể khi tham số được cung cấp.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng `getopts`:

### Ví dụ 1: Sử dụng với tham số đơn giản
```bash
#!/bin/bash

while getopts "a:b:c:" opt; do
  case $opt in
    a) echo "Option A: $OPTARG" ;;
    b) echo "Option B: $OPTARG" ;;
    c) echo "Option C: $OPTARG" ;;
    *) echo "Invalid option" ;;
  esac
done
```
Chạy script với: `./script.sh -a value1 -b value2 -c value3`

### Ví dụ 2: Kiểm tra tham số
```bash
#!/bin/bash

while getopts "f:" opt; do
  case $opt in
    f) echo "File: $OPTARG" ;;
    *) echo "Usage: $0 -f filename" ;;
  esac
done
```
Chạy script với: `./script.sh -f myfile.txt`

### Ví dụ 3: Tham số mặc định
```bash
#!/bin/bash

verbose=0

while getopts "v" opt; do
  case $opt in
    v) verbose=1 ;;
    *) echo "Usage: $0 [-v]" ;;
  esac
done

if [ $verbose -eq 1 ]; then
  echo "Verbose mode is ON"
fi
```
Chạy script với: `./script.sh -v`

## Mẹo
- **Sử dụng tham số mặc định**: Đặt giá trị mặc định cho các biến để tránh lỗi khi không có tham số.
- **Kiểm tra tham số**: Luôn kiểm tra xem tham số có hợp lệ hay không để đảm bảo script chạy đúng.
- **Giúp người dùng**: Cung cấp thông tin hướng dẫn khi tham số không hợp lệ để người dùng biết cách sử dụng đúng.

Lệnh `getopts` là một công cụ mạnh mẽ giúp quản lý tham số dòng lệnh trong các script Bash, giúp cho việc phát triển trở nên dễ dàng và hiệu quả hơn.