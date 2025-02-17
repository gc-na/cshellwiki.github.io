# [Linux] Bash case: Xử lý các lựa chọn điều kiện

## Overview
Lệnh `case` trong Bash được sử dụng để thực hiện các lựa chọn điều kiện dựa trên giá trị của một biến. Nó cho phép bạn kiểm tra một giá trị và thực hiện các hành động khác nhau tùy thuộc vào giá trị đó, tương tự như cấu trúc `switch` trong các ngôn ngữ lập trình khác.

## Usage
Cú pháp cơ bản của lệnh `case` như sau:

```bash
case [biến] in
    [mẫu1])
        [lệnh1]
        ;;
    [mẫu2])
        [lệnh2]
        ;;
    *)
        [lệnh_mặc_dịnh]
        ;;
esac
```

## Common Options
- `*)`: Mẫu mặc định, sẽ được thực hiện nếu không có mẫu nào khớp.
- `;;`: Kết thúc một khối lệnh cho một mẫu.

## Common Examples

### Ví dụ 1: Kiểm tra ngày trong tuần
```bash
day="Thứ Hai"
case $day in
    "Thứ Hai")
        echo "Hôm nay là đầu tuần."
        ;;
    "Thứ Sáu")
        echo "Hôm nay là cuối tuần."
        ;;
    *)
        echo "Hôm nay là một ngày khác."
        ;;
esac
```

### Ví dụ 2: Kiểm tra số
```bash
number=3
case $number in
    1)
        echo "Số một."
        ;;
    2)
        echo "Số hai."
        ;;
    3)
        echo "Số ba."
        ;;
    *)
        echo "Số không xác định."
        ;;
esac
```

### Ví dụ 3: Kiểm tra loại tệp
```bash
file="document.txt"
case $file in
    *.txt)
        echo "Đây là một tệp văn bản."
        ;;
    *.jpg | *.png)
        echo "Đây là một tệp hình ảnh."
        ;;
    *)
        echo "Loại tệp không xác định."
        ;;
esac
```

## Tips
- Sử dụng `case` khi bạn cần kiểm tra nhiều giá trị khác nhau cho một biến, điều này giúp mã của bạn gọn gàng và dễ đọc hơn.
- Đảm bảo rằng mỗi mẫu kết thúc bằng `;;` để tránh lỗi trong quá trình thực thi.
- Bạn có thể sử dụng nhiều mẫu cho một lệnh bằng cách sử dụng dấu `|` để phân tách chúng, như trong ví dụ kiểm tra loại tệp.