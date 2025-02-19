# [Hệ điều hành Unix] C Shell (csh) foreach: Lặp qua danh sách

## Overview
Lệnh `foreach` trong C Shell (csh) được sử dụng để lặp qua một danh sách các giá trị và thực hiện một tập hợp các lệnh cho mỗi giá trị trong danh sách đó. Đây là một công cụ hữu ích để tự động hóa các tác vụ lặp đi lặp lại.

## Usage
Cú pháp cơ bản của lệnh `foreach` như sau:

```
foreach variable (list)
    commands
end
```

## Common Options
Lệnh `foreach` không có nhiều tùy chọn như các lệnh khác, nhưng bạn có thể sử dụng một số tùy chọn cơ bản như:
- `variable`: Tên biến sẽ nhận giá trị từ danh sách.
- `list`: Danh sách các giá trị mà bạn muốn lặp qua.

## Common Examples

### Ví dụ 1: Lặp qua một danh sách số
```csh
foreach i (1 2 3 4 5)
    echo "Số hiện tại là: $i"
end
```

### Ví dụ 2: Lặp qua các tệp trong thư mục
```csh
foreach file (*.txt)
    echo "Đang xử lý tệp: $file"
end
```

### Ví dụ 3: Lặp qua các tham số đầu vào
```csh
foreach arg ($*)
    echo "Tham số: $arg"
end
```

## Tips
- Hãy chắc chắn rằng danh sách bạn cung cấp không chứa các ký tự đặc biệt mà có thể gây ra lỗi.
- Sử dụng `echo` để kiểm tra giá trị của biến trong quá trình lặp để đảm bảo rằng nó hoạt động như mong muốn.
- Bạn có thể kết hợp `foreach` với các lệnh khác để tạo ra các kịch bản phức tạp hơn.