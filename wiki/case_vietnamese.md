# [Hệ điều hành] C Shell (csh) case: Phân loại các lựa chọn

## Overview
Lệnh `case` trong C Shell (csh) được sử dụng để kiểm tra một biến và thực hiện các hành động khác nhau dựa trên giá trị của biến đó. Nó rất hữu ích trong việc xử lý các lựa chọn và điều kiện trong các script.

## Usage
Cú pháp cơ bản của lệnh `case` như sau:
```
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
- `*)`: Đây là lựa chọn mặc định, được thực hiện nếu không có giá trị nào khớp với các trường hợp đã chỉ định.
- `;;`: Dùng để kết thúc một trường hợp và chuyển sang trường hợp tiếp theo.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `case`:

### Ví dụ 1: Phân loại số
```csh
set num = 2
switch ($num)
    case 1:
        echo "Số là 1"
        breaksw
    case 2:
        echo "Số là 2"
        breaksw
    case 3:
        echo "Số là 3"
        breaksw
    default:
        echo "Số không nằm trong danh sách"
endsw
```

### Ví dụ 2: Phân loại tháng
```csh
set month = "Tháng 5"
case ($month) in
    "Tháng 1" | "Tháng 2" | "Tháng 3")
        echo "Quý 1"
        ;;
    "Tháng 4" | "Tháng 5" | "Tháng 6")
        echo "Quý 2"
        ;;
    *)
        echo "Không thuộc quý nào"
        ;;
esac
```

### Ví dụ 3: Kiểm tra loại tệp
```csh
set file = "document.txt"
case ($file) in
    *.txt)
        echo "Đây là tệp văn bản"
        ;;
    *.jpg | *.png)
        echo "Đây là tệp hình ảnh"
        ;;
    *)
        echo "Loại tệp không xác định"
        ;;
esac
```

## Tips
- Sử dụng `case` để làm cho mã của bạn dễ đọc hơn khi xử lý nhiều điều kiện.
- Đảm bảo rằng mỗi trường hợp kết thúc bằng `;;` để tránh lỗi trong script.
- Sử dụng lựa chọn mặc định `*` để xử lý các trường hợp không lường trước được.