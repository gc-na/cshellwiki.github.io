# [Linux] Bash foreach sử dụng: Lặp qua danh sách

## Overview
Lệnh `foreach` trong Bash cho phép bạn lặp qua một danh sách các phần tử và thực hiện một lệnh hoặc một chuỗi lệnh cho mỗi phần tử trong danh sách đó. Đây là một công cụ hữu ích để tự động hóa các tác vụ lặp lại mà không cần phải viết nhiều dòng lệnh.

## Usage
Cú pháp cơ bản của lệnh `foreach` như sau:
```bash
foreach variable (list)
    command
end
```

## Common Options
Lệnh `foreach` không có nhiều tùy chọn như một số lệnh khác, nhưng bạn có thể sử dụng các biến để tùy chỉnh hành vi của nó. Một số tùy chọn phổ biến bao gồm:
- `-n`: Không hiển thị lệnh đang thực hiện.
- `-p`: Cho phép người dùng nhập vào trong mỗi vòng lặp.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `foreach`:

### Ví dụ 1: Lặp qua danh sách số
```bash
foreach i (1 2 3 4 5)
    echo "Số hiện tại là: $i"
end
```

### Ví dụ 2: Lặp qua các tệp trong thư mục
```bash
foreach file (*)
    echo "Tệp hiện tại là: $file"
end
```

### Ví dụ 3: Chạy lệnh cho mỗi tệp
```bash
foreach file (*.txt)
    cat $file
end
```

## Tips
- Sử dụng `foreach` khi bạn cần thực hiện các lệnh lặp lại trên một danh sách cụ thể.
- Hãy chắc chắn rằng danh sách bạn đang lặp qua không rỗng để tránh lỗi.
- Kết hợp `foreach` với các lệnh khác như `grep`, `awk` để xử lý dữ liệu một cách hiệu quả hơn.