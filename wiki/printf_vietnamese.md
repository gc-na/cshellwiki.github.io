# [Linux] Bash printf Cách sử dụng: In định dạng văn bản

## Tổng quan
Lệnh `printf` trong Bash được sử dụng để in ra văn bản theo định dạng cụ thể. Nó cho phép người dùng kiểm soát cách mà dữ liệu được hiển thị, bao gồm cả việc định dạng số, chuỗi và các kiểu dữ liệu khác.

## Cách sử dụng
Cú pháp cơ bản của lệnh `printf` như sau:
```bash
printf [options] [arguments]
```

## Các tùy chọn phổ biến
- `-v var`: Gán kết quả vào biến `var` thay vì in ra.
- `--help`: Hiển thị thông tin trợ giúp về lệnh.
- `--version`: Hiển thị phiên bản của lệnh `printf`.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `printf`:

### In một chuỗi đơn giản
```bash
printf "Xin chào, thế giới!\n"
```

### Định dạng số
```bash
printf "Số nguyên: %d\n" 42
```

### Định dạng số thực
```bash
printf "Số thực: %.2f\n" 3.14159
```

### In nhiều đối số
```bash
printf "Tên: %s, Tuổi: %d\n" "Nguyễn Văn A" 30
```

### Gán kết quả vào biến
```bash
printf -v result "Kết quả: %.2f" 123.456
echo "$result"
```

## Mẹo
- Sử dụng `\n` để thêm dòng mới trong chuỗi in ra.
- Kiểm tra các định dạng khác nhau như `%s` cho chuỗi, `%d` cho số nguyên, và `%.2f` cho số thực để có kết quả chính xác.
- Thử nghiệm với các tùy chọn khác nhau để tìm ra cách định dạng phù hợp nhất cho nhu cầu của bạn.