# [Linux] Bash ls Cách sử dụng: Liệt kê các tệp và thư mục

## Tổng quan
Lệnh `ls` trong Bash được sử dụng để liệt kê các tệp và thư mục trong một thư mục cụ thể. Đây là một trong những lệnh cơ bản và thường xuyên được sử dụng trong môi trường dòng lệnh.

## Cách sử dụng
Cú pháp cơ bản của lệnh `ls` như sau:
```
ls [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-l`: Hiển thị thông tin chi tiết về các tệp và thư mục, bao gồm quyền truy cập, số lượng liên kết, chủ sở hữu, kích thước và thời gian sửa đổi.
- `-a`: Hiển thị tất cả các tệp, bao gồm cả các tệp ẩn (tệp bắt đầu bằng dấu chấm).
- `-h`: Hiển thị kích thước tệp theo định dạng dễ đọc (như KB, MB).
- `-R`: Liệt kê các thư mục và tệp trong tất cả các thư mục con.
- `-t`: Sắp xếp các tệp theo thời gian sửa đổi, với tệp mới nhất ở trên cùng.

## Ví dụ phổ biến
- Liệt kê các tệp trong thư mục hiện tại:
  ```bash
  ls
  ```

- Liệt kê tất cả các tệp, bao gồm cả tệp ẩn:
  ```bash
  ls -a
  ```

- Hiển thị thông tin chi tiết về các tệp:
  ```bash
  ls -l
  ```

- Hiển thị kích thước tệp theo định dạng dễ đọc:
  ```bash
  ls -lh
  ```

- Liệt kê các tệp trong thư mục con:
  ```bash
  ls -R
  ```

- Sắp xếp các tệp theo thời gian sửa đổi:
  ```bash
  ls -lt
  ```

## Mẹo
- Sử dụng `ls -lh` để dễ dàng đọc kích thước tệp, đặc biệt khi làm việc với các tệp lớn.
- Kết hợp nhiều tùy chọn, ví dụ: `ls -la` để xem tất cả các tệp với thông tin chi tiết.
- Nếu bạn muốn tìm kiếm tệp theo tên, hãy kết hợp với lệnh `grep`, ví dụ: `ls | grep "tên_tệp"`.