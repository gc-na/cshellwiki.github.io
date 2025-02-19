# [Hệ điều hành] C Shell (csh) if: Kiểm tra điều kiện

## Overview
Lệnh `if` trong C Shell (csh) được sử dụng để kiểm tra các điều kiện và thực hiện các lệnh dựa trên kết quả của các điều kiện đó. Nó cho phép người dùng thực hiện các hành động khác nhau tùy thuộc vào việc điều kiện có đúng hay không.

## Usage
Cú pháp cơ bản của lệnh `if` như sau:

```
if ( điều kiện ) then
    lệnh
endif
```

## Common Options
- `then`: Bắt đầu khối lệnh sẽ được thực hiện nếu điều kiện đúng.
- `endif`: Kết thúc khối lệnh `if`.
- `else`: Thực hiện khối lệnh khác nếu điều kiện không đúng.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `if`:

### Ví dụ 1: Kiểm tra một biến
```csh
set var = 5
if ( $var == 5 ) then
    echo "Biến var có giá trị là 5."
endif
```

### Ví dụ 2: Kiểm tra tệp tồn tại
```csh
if ( -e "file.txt" ) then
    echo "Tệp file.txt tồn tại."
else
    echo "Tệp file.txt không tồn tại."
endif
```

### Ví dụ 3: Kiểm tra một điều kiện số
```csh
set num = 10
if ( $num > 5 ) then
    echo "Số lớn hơn 5."
else
    echo "Số không lớn hơn 5."
endif
```

## Tips
- Luôn sử dụng dấu cách đúng cách giữa các phần của lệnh `if` để tránh lỗi cú pháp.
- Có thể sử dụng nhiều điều kiện kết hợp với `&&` (và) hoặc `||` (hoặc) để kiểm tra nhiều điều kiện cùng một lúc.
- Đảm bảo rằng bạn đã đóng khối lệnh `if` bằng `endif` để tránh lỗi trong chương trình.