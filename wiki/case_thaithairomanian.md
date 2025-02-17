# [Bash] Bash case sử dụng: Xử lý điều kiện trong shell script

## Overview
Lệnh `case` trong Bash được sử dụng để kiểm tra một biến và thực hiện các hành động khác nhau dựa trên giá trị của biến đó. Đây là một cách hiệu quả để xử lý nhiều điều kiện mà không cần phải sử dụng nhiều câu lệnh `if`.

## Usage
Cú pháp cơ bản của lệnh `case` như sau:

```bash
case [biến] in
    [giá trị1])
        [lệnh1]
        ;;
    [giá trị2])
        [lệnh2]
        ;;
    *)
        [lệnh_mặc_định]
        ;;
esac
```

## Common Options
- Không có tùy chọn cụ thể cho lệnh `case`, nhưng bạn có thể sử dụng các ký tự đại diện như `*` và `?` để khớp với nhiều giá trị khác nhau.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `case`:

### Ví dụ 1: Kiểm tra biến
```bash
#!/bin/bash
echo "Nhập số từ 1 đến 3:"
read number

case $number in
    1)
        echo "Bạn đã chọn số một."
        ;;
    2)
        echo "Bạn đã chọn số hai."
        ;;
    3)
        echo "Bạn đã chọn số ba."
        ;;
    *)
        echo "Số không hợp lệ."
        ;;
esac
```

### Ví dụ 2: Kiểm tra loại tệp
```bash
#!/bin/bash
echo "Nhập tên tệp:"
read filename

case $filename in
    *.txt)
        echo "Đây là tệp văn bản."
        ;;
    *.jpg | *.png)
        echo "Đây là tệp hình ảnh."
        ;;
    *)
        echo "Loại tệp không xác định."
        ;;
esac
```

### Ví dụ 3: Lựa chọn hành động
```bash
#!/bin/bash
echo "Chọn hành động: (start/stop/restart)"
read action

case $action in
    start)
        echo "Bắt đầu dịch vụ."
        ;;
    stop)
        echo "Dừng dịch vụ."
        ;;
    restart)
        echo "Khởi động lại dịch vụ."
        ;;
    *)
        echo "Hành động không hợp lệ."
        ;;
esac
```

## Tips
- Sử dụng `case` khi bạn có nhiều điều kiện để kiểm tra, điều này giúp mã của bạn dễ đọc hơn so với việc sử dụng nhiều câu lệnh `if`.
- Đảm bảo sử dụng `;;` để kết thúc mỗi khối lệnh trong `case`.
- Bạn có thể kết hợp nhiều giá trị cho một khối lệnh bằng cách sử dụng dấu `|` để phân tách các giá trị.