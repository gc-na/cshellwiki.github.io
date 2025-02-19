# [Hệ điều hành] C Shell (csh) switch: Chuyển đổi giữa các lựa chọn

## Overview
Lệnh `switch` trong C Shell (csh) được sử dụng để thực hiện các lựa chọn điều kiện trong một kịch bản. Nó cho phép người dùng kiểm tra giá trị của một biến và thực hiện các hành động khác nhau dựa trên giá trị đó.

## Usage
Cú pháp cơ bản của lệnh `switch` như sau:
```
switch (biến)
    case giá_trị_1:
        lệnh_1
        breaksw
    case giá_trị_2:
        lệnh_2
        breaksw
    default:
        lệnh_mặc_dịnh
        breaksw
endsw
```

## Common Options
- `case`: Được sử dụng để xác định một giá trị mà biến có thể khớp.
- `breaksw`: Kết thúc một trường hợp và thoát khỏi lệnh `switch`.
- `default`: Được sử dụng để chỉ định hành động mặc định nếu không có trường hợp nào khớp.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `switch`:

### Ví dụ 1: Kiểm tra ngày trong tuần
```csh
set day = "Thứ Hai"
switch ($day)
    case "Thứ Hai":
        echo "Hôm nay là thứ Hai."
        breaksw
    case "Thứ Ba":
        echo "Hôm nay là thứ Ba."
        breaksw
    default:
        echo "Hôm nay không phải là thứ Hai hoặc thứ Ba."
        breaksw
endsw
```

### Ví dụ 2: Kiểm tra số
```csh
set num = 2
switch ($num)
    case 1:
        echo "Số là một."
        breaksw
    case 2:
        echo "Số là hai."
        breaksw
    case 3:
        echo "Số là ba."
        breaksw
    default:
        echo "Số không nằm trong khoảng 1 đến 3."
        breaksw
endsw
```

### Ví dụ 3: Kiểm tra loại tệp
```csh
set file_type = "pdf"
switch ($file_type)
    case "txt":
        echo "Đây là tệp văn bản."
        breaksw
    case "pdf":
        echo "Đây là tệp PDF."
        breaksw
    case "jpg":
        echo "Đây là tệp hình ảnh."
        breaksw
    default:
        echo "Loại tệp không xác định."
        breaksw
endsw
```

## Tips
- Sử dụng `breaksw` để đảm bảo rằng chỉ một trường hợp được thực hiện và không tiếp tục kiểm tra các trường hợp khác.
- Đặt `default` ở cuối để xử lý các trường hợp không khớp.
- Đảm bảo rằng biến được kiểm tra đã được khởi tạo trước khi sử dụng lệnh `switch`.