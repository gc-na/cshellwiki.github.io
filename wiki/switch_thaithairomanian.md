# [Bash] Bash switch sử dụng: Chuyển đổi giữa các tùy chọn

## Overview
Lệnh `switch` trong Bash cho phép người dùng chuyển đổi giữa các tùy chọn hoặc điều kiện khác nhau trong một kịch bản. Mặc dù không phải là một lệnh có sẵn trong Bash, nó thường được sử dụng trong ngữ cảnh của các lệnh điều kiện như `case` để thực hiện các hành động khác nhau dựa trên giá trị của một biến.

## Usage
Cú pháp cơ bản của lệnh `switch` có thể được biểu diễn như sau:

```bash
case [biến] in
    [giá trị1])
        [lệnh1]
        ;;
    [giá trị2])
        [lệnh2]
        ;;
    *)
        [lệnh mặc định]
        ;;
esac
```

## Common Options
- `case`: Bắt đầu một khối điều kiện.
- `in`: Chỉ định các giá trị mà biến có thể nhận.
- `;;`: Kết thúc một trường hợp.
- `*`: Trường hợp mặc định nếu không có giá trị nào khớp.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `switch` trong Bash:

### Ví dụ 1: Chọn hành động dựa trên ngày trong tuần
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

### Ví dụ 2: Kiểm tra loại tệp
```bash
file="document.txt"

case $file in
    *.txt)
        echo "Đây là tệp văn bản."
        ;;
    *.jpg)
        echo "Đây là tệp hình ảnh."
        ;;
    *)
        echo "Loại tệp không xác định."
        ;;
esac
```

### Ví dụ 3: Chọn món ăn
```bash
food="pizza"

case $food in
    "pizza")
        echo "Bạn đã chọn pizza."
        ;;
    "salad")
        echo "Bạn đã chọn salad."
        ;;
    *)
        echo "Món ăn không có trong danh sách."
        ;;
esac
```

## Tips
- Sử dụng `case` khi bạn có nhiều điều kiện để kiểm tra, giúp mã dễ đọc hơn.
- Đảm bảo sử dụng `;;` để kết thúc mỗi trường hợp, tránh lỗi cú pháp.
- Sử dụng trường hợp mặc định `*` để xử lý các giá trị không mong muốn hoặc không xác định.