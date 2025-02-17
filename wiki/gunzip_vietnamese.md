# [Linux] Bash gunzip Cách sử dụng: Giải nén tệp tin gzip

## Tổng quan
Lệnh `gunzip` được sử dụng để giải nén các tệp tin nén bằng định dạng gzip. Nó giúp bạn khôi phục lại các tệp tin đã được nén, cho phép bạn truy cập nội dung gốc của chúng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `gunzip` như sau:
```
gunzip [tùy chọn] [tệp tin]
```

## Tùy chọn phổ biến
- `-c`: Giải nén tệp tin và xuất kết quả ra stdout (màn hình).
- `-f`: Buộc giải nén, ngay cả khi tệp tin đã tồn tại.
- `-k`: Giữ lại tệp tin gốc sau khi giải nén.
- `-r`: Giải nén tất cả các tệp tin trong thư mục con.

## Ví dụ phổ biến
- Giải nén một tệp tin gzip đơn giản:
  ```bash
  gunzip file.txt.gz
  ```

- Giải nén và giữ lại tệp tin gốc:
  ```bash
  gunzip -k file.txt.gz
  ```

- Giải nén tất cả các tệp tin trong thư mục:
  ```bash
  gunzip *.gz
  ```

- Giải nén và xuất kết quả ra stdout:
  ```bash
  gunzip -c file.txt.gz > file.txt
  ```

## Mẹo
- Sử dụng tùy chọn `-k` nếu bạn muốn giữ lại tệp tin nén gốc để sử dụng sau này.
- Kiểm tra dung lượng tệp tin sau khi giải nén để đảm bảo bạn có đủ không gian lưu trữ.
- Nếu bạn không chắc chắn về tệp tin nào sẽ bị ghi đè, hãy sử dụng tùy chọn `-f` một cách thận trọng.