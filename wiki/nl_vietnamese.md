# [Linux] Bash nl Cách sử dụng: Đánh số dòng trong tệp tin

## Overview
Lệnh `nl` trong Bash được sử dụng để đánh số các dòng trong một tệp tin. Nó cho phép người dùng dễ dàng theo dõi vị trí của các dòng trong tệp, điều này rất hữu ích khi làm việc với các tệp văn bản lớn.

## Usage
Cú pháp cơ bản của lệnh `nl` như sau:
```
nl [options] [arguments]
```

## Common Options
- `-b` : Chỉ định cách đánh số dòng (ví dụ: `-b a` để đánh số tất cả các dòng).
- `-f` : Chỉ định số dòng đầu tiên để bắt đầu đánh số.
- `-n` : Chỉ định cách hiển thị số dòng (ví dụ: `-n ln` để hiển thị số dòng bên trái).
- `-w` : Chỉ định chiều rộng của số dòng.

## Common Examples
1. Đánh số tất cả các dòng trong một tệp tin:
   ```bash
   nl filename.txt
   ```

2. Đánh số chỉ các dòng không trống:
   ```bash
   nl -b t filename.txt
   ```

3. Đánh số dòng bắt đầu từ dòng thứ 5:
   ```bash
   nl -f 5 filename.txt
   ```

4. Thay đổi cách hiển thị số dòng:
   ```bash
   nl -n ln filename.txt
   ```

## Tips
- Sử dụng `nl` kết hợp với các lệnh khác như `grep` hoặc `less` để dễ dàng tìm kiếm và xem các dòng đã được đánh số.
- Kiểm tra các tùy chọn khác nhau để tùy chỉnh cách hiển thị số dòng theo nhu cầu của bạn.
- Đọc tài liệu hướng dẫn bằng cách sử dụng `man nl` để tìm hiểu thêm về các tùy chọn và cách sử dụng.