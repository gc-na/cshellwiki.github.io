# [Linux] Bash readonly cách sử dụng: Đặt biến không thể thay đổi

## Tổng quan
Lệnh `readonly` trong Bash được sử dụng để đánh dấu một biến là không thể thay đổi. Khi một biến được đánh dấu là `readonly`, bạn không thể gán giá trị mới cho nó trong phiên làm việc hiện tại, giúp bảo vệ các giá trị quan trọng khỏi việc bị thay đổi.

## Cú pháp
Cú pháp cơ bản của lệnh `readonly` như sau:
```bash
readonly [tùy chọn] [biến]
```

## Các tùy chọn phổ biến
- `-p`: Hiển thị danh sách tất cả các biến đã được đánh dấu là `readonly`.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `readonly`:

### Ví dụ 1: Đánh dấu biến là readonly
```bash
my_var="Giá trị ban đầu"
readonly my_var
```

### Ví dụ 2: Cố gắng thay đổi giá trị của biến readonly
```bash
my_var="Giá trị mới"  # Lệnh này sẽ gây ra lỗi
```

### Ví dụ 3: Hiển thị các biến readonly
```bash
readonly -p
```

## Mẹo
- Sử dụng `readonly` cho các biến quan trọng để tránh việc vô tình thay đổi giá trị của chúng.
- Kiểm tra các biến readonly thường xuyên để đảm bảo rằng các giá trị quan trọng không bị thay đổi trong quá trình thực thi script.
- Bạn có thể sử dụng `declare -r` thay thế cho `readonly`, vì chúng có chức năng tương tự.