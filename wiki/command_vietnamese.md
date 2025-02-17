# [Linux] Bash command tìm kiếm: Tìm kiếm tệp tin và thư mục

## Overview
Lệnh `find` trong Bash được sử dụng để tìm kiếm tệp tin và thư mục trong hệ thống tệp. Nó cho phép người dùng tìm kiếm theo nhiều tiêu chí khác nhau như tên, kích thước, thời gian sửa đổi, và nhiều thuộc tính khác.

## Usage
Cú pháp cơ bản của lệnh `find` như sau:

```bash
find [đường_dẫn] [tùy_chọn] [biểu_thức]
```

## Common Options
- `-name`: Tìm tệp tin theo tên.
- `-type`: Chỉ định loại tệp (ví dụ: `f` cho tệp tin, `d` cho thư mục).
- `-size`: Tìm tệp tin theo kích thước.
- `-mtime`: Tìm tệp tin theo thời gian sửa đổi (ngày).
- `-exec`: Thực hiện một lệnh trên các tệp tin tìm thấy.

## Common Examples
- Tìm tất cả các tệp tin có đuôi `.txt` trong thư mục hiện tại:

```bash
find . -name "*.txt"
```

- Tìm tất cả các thư mục trong `/home/user`:

```bash
find /home/user -type d
```

- Tìm các tệp tin lớn hơn 1MB trong thư mục `/var`:

```bash
find /var -type f -size +1M
```

- Tìm các tệp tin đã được sửa đổi trong 7 ngày qua:

```bash
find . -mtime -7
```

- Thực hiện lệnh `rm` để xóa tất cả các tệp tin `.log` trong thư mục hiện tại:

```bash
find . -name "*.log" -exec rm {} \;
```

## Tips
- Sử dụng `-print` để hiển thị kết quả tìm kiếm nếu bạn không sử dụng `-exec`.
- Kết hợp nhiều tùy chọn để tinh chỉnh kết quả tìm kiếm.
- Luôn kiểm tra kết quả tìm kiếm trước khi thực hiện các lệnh xóa để tránh mất dữ liệu không mong muốn.