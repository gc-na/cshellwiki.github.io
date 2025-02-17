# [Linux] Bash grep Cách sử dụng: Tìm kiếm văn bản trong tệp

## Tổng quan
Lệnh `grep` là một công cụ mạnh mẽ trong Bash, dùng để tìm kiếm các chuỗi văn bản trong tệp hoặc đầu ra của các lệnh khác. Nó cho phép người dùng lọc thông tin và tìm kiếm các mẫu cụ thể một cách nhanh chóng và hiệu quả.

## Cách sử dụng
Cú pháp cơ bản của lệnh `grep` như sau:

```bash
grep [options] [arguments]
```

## Các tùy chọn phổ biến
- `-i`: Bỏ qua sự phân biệt chữ hoa chữ thường trong quá trình tìm kiếm.
- `-v`: In ra các dòng không chứa mẫu tìm kiếm.
- `-r`: Tìm kiếm đệ quy trong các thư mục.
- `-n`: Hiển thị số dòng của kết quả tìm kiếm.
- `-l`: Chỉ hiển thị tên tệp chứa mẫu tìm kiếm.

## Ví dụ thường gặp
- Tìm kiếm một chuỗi trong một tệp:

```bash
grep "chuỗi cần tìm" ten_tap.txt
```

- Tìm kiếm không phân biệt chữ hoa chữ thường:

```bash
grep -i "chuỗi cần tìm" ten_tap.txt
```

- Tìm kiếm trong tất cả các tệp trong thư mục hiện tại và các thư mục con:

```bash
grep -r "chuỗi cần tìm" .
```

- Hiển thị số dòng của kết quả tìm kiếm:

```bash
grep -n "chuỗi cần tìm" ten_tap.txt
```

- Tìm kiếm và chỉ hiển thị tên tệp chứa mẫu:

```bash
grep -l "chuỗi cần tìm" *.txt
```

## Mẹo
- Sử dụng `grep` kết hợp với các lệnh khác bằng cách sử dụng dấu `|` để lọc đầu ra, ví dụ: `ls -l | grep "tên_tệp"`.
- Để tìm kiếm nhiều mẫu cùng lúc, bạn có thể sử dụng `-e`, ví dụ: `grep -e "mẫu1" -e "mẫu2" ten_tap.txt`.
- Lưu ý rằng `grep` có thể làm việc với các tệp lớn, nhưng nếu bạn cần tìm kiếm trong tệp rất lớn, hãy cân nhắc sử dụng `grep` với tùy chọn `-F` để tăng tốc độ tìm kiếm.