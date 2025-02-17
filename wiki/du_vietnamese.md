# [Linux] Bash du: Đo kích thước thư mục và tệp

## Overview
Lệnh `du` (disk usage) được sử dụng để đo kích thước của thư mục và tệp trong hệ thống tệp. Nó giúp người dùng xác định dung lượng mà các tệp và thư mục đang chiếm trên đĩa cứng.

## Usage
Cú pháp cơ bản của lệnh `du` như sau:
```bash
du [options] [arguments]
```

## Common Options
- `-h`: Hiển thị kích thước theo định dạng dễ đọc (KB, MB, GB).
- `-s`: Tóm tắt kích thước của thư mục mà không liệt kê các tệp con.
- `-a`: Hiển thị kích thước của cả tệp và thư mục.
- `-c`: Tính tổng kích thước của tất cả các tệp và thư mục được liệt kê.

## Common Examples
- Đo kích thước của thư mục hiện tại:
```bash
du
```

- Đo kích thước của thư mục hiện tại và hiển thị kết quả theo định dạng dễ đọc:
```bash
du -h
```

- Tóm tắt kích thước của một thư mục cụ thể:
```bash
du -sh /path/to/directory
```

- Hiển thị kích thước của tất cả các tệp và thư mục trong thư mục hiện tại:
```bash
du -ah
```

- Tính tổng kích thước của tất cả các thư mục con trong thư mục hiện tại:
```bash
du -ch *
```

## Tips
- Sử dụng tùy chọn `-h` để dễ dàng đọc kích thước, đặc biệt khi làm việc với các thư mục lớn.
- Kết hợp `du` với lệnh `sort` để sắp xếp kết quả theo kích thước:
```bash
du -h | sort -h
```
- Thường xuyên kiểm tra kích thước của các thư mục để quản lý không gian đĩa hiệu quả hơn.