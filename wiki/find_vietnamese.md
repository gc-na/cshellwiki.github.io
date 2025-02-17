# [Linux] Bash find cách sử dụng: Tìm kiếm tên tệp

## Tổng quan
Lệnh `find` trong Bash được sử dụng để tìm kiếm các tệp và thư mục trong hệ thống tệp dựa trên các tiêu chí nhất định như tên, kích thước, thời gian sửa đổi, và nhiều thuộc tính khác.

## Cách sử dụng
Cú pháp cơ bản của lệnh `find` như sau:
```bash
find [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-name`: Tìm các tệp có tên cụ thể.
- `-type`: Chỉ định loại tệp (ví dụ: `f` cho tệp thường, `d` cho thư mục).
- `-size`: Tìm các tệp dựa trên kích thước.
- `-mtime`: Tìm các tệp đã được sửa đổi trong một khoảng thời gian nhất định.
- `-exec`: Thực thi một lệnh trên các tệp tìm thấy.

## Ví dụ thường gặp
1. Tìm tất cả các tệp có đuôi `.txt` trong thư mục hiện tại:
   ```bash
   find . -name "*.txt"
   ```

2. Tìm tất cả các thư mục trong thư mục `/home/user`:
   ```bash
   find /home/user -type d
   ```

3. Tìm các tệp lớn hơn 1MB:
   ```bash
   find . -size +1M
   ```

4. Tìm các tệp đã được sửa đổi trong 7 ngày qua:
   ```bash
   find . -mtime -7
   ```

5. Xóa tất cả các tệp `.tmp` trong thư mục hiện tại:
   ```bash
   find . -name "*.tmp" -exec rm {} \;
   ```

## Mẹo
- Sử dụng `-print` để hiển thị kết quả tìm kiếm nếu bạn không sử dụng `-exec`.
- Kết hợp nhiều tùy chọn để thu hẹp kết quả tìm kiếm.
- Cẩn thận khi sử dụng `-exec` với lệnh xóa, hãy chắc chắn rằng bạn đã kiểm tra kết quả trước khi thực hiện.