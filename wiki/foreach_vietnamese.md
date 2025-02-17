# [Linux] Bash foreach cách sử dụng: Lặp qua các phần tử

## Tổng quan
Lệnh `foreach` trong Bash được sử dụng để lặp qua một danh sách các phần tử và thực hiện một lệnh hoặc một tập hợp các lệnh cho mỗi phần tử trong danh sách đó. Đây là một công cụ hữu ích để tự động hóa các tác vụ lặp đi lặp lại.

## Cú pháp
Cú pháp cơ bản của lệnh `foreach` như sau:
```bash
foreach variable (list)
    command
end
```

## Các tùy chọn phổ biến
- `variable`: Tên biến sẽ lưu trữ giá trị của từng phần tử trong danh sách.
- `list`: Danh sách các phần tử mà bạn muốn lặp qua.
- `command`: Lệnh sẽ được thực thi cho mỗi phần tử trong danh sách.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `foreach`:

### Ví dụ 1: Lặp qua một danh sách số
```bash
foreach i (1 2 3 4 5)
    echo "Số hiện tại là: $i"
end
```

### Ví dụ 2: Lặp qua các tệp trong thư mục
```bash
foreach file (*.txt)
    echo "Đang xử lý tệp: $file"
end
```

### Ví dụ 3: Thực hiện lệnh trên nhiều thư mục
```bash
foreach dir (dir1 dir2 dir3)
    cd $dir
    ls
    cd ..
end
```

## Mẹo
- Hãy chắc chắn rằng danh sách bạn cung cấp cho lệnh `foreach` không rỗng, nếu không, lệnh sẽ không thực hiện gì cả.
- Sử dụng các lệnh kiểm tra (như `if`) bên trong vòng lặp để xử lý các điều kiện khác nhau cho từng phần tử.
- Thực hành với các lệnh khác nhau để làm quen với cách `foreach` hoạt động trong các tình huống khác nhau.