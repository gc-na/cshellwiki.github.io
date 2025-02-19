# [Hệ điều hành Unix] C Shell (csh) while: Thực hiện lặp lại một khối lệnh

## Overview
Lệnh `while` trong C Shell (csh) được sử dụng để thực hiện một khối lệnh nhiều lần miễn là điều kiện được chỉ định là đúng. Điều này rất hữu ích khi bạn cần lặp lại một tác vụ cho đến khi một điều kiện nào đó không còn đúng nữa.

## Usage
Cú pháp cơ bản của lệnh `while` như sau:

```
while ( điều kiện )
    lệnh
end
```

## Common Options
Lệnh `while` không có nhiều tùy chọn như các lệnh khác, nhưng điều kiện trong lệnh có thể sử dụng các biểu thức điều kiện cơ bản như:

- `-eq`: Kiểm tra xem hai giá trị có bằng nhau không.
- `-ne`: Kiểm tra xem hai giá trị có khác nhau không.
- `-lt`: Kiểm tra xem giá trị bên trái có nhỏ hơn giá trị bên phải không.
- `-gt`: Kiểm tra xem giá trị bên trái có lớn hơn giá trị bên phải không.

## Common Examples

### Ví dụ 1: Lặp qua số từ 1 đến 5
```csh
set i = 1
while ( $i <= 5 )
    echo "Số hiện tại là: $i"
    @ i++
end
```

### Ví dụ 2: Đọc đầu vào cho đến khi người dùng nhập "exit"
```csh
set input = ""
while ( "$input" != "exit" )
    echo "Nhập một từ (hoặc 'exit' để thoát):"
    set input = $<
end
```

### Ví dụ 3: Lặp cho đến khi một tệp tồn tại
```csh
set filename = "test.txt"
while ( ! -e $filename )
    echo "Tệp chưa tồn tại, đang chờ..."
    sleep 2
end
echo "Tệp đã tồn tại!"
```

## Tips
- Đảm bảo rằng điều kiện trong lệnh `while` sẽ có khả năng trở thành sai để tránh việc lặp vô hạn.
- Sử dụng lệnh `sleep` trong vòng lặp để giảm tải cho CPU nếu cần thiết.
- Kiểm tra kỹ các biến và điều kiện trước khi sử dụng để đảm bảo chúng hoạt động như mong muốn.