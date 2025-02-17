# [Linux] Bash xz Cách sử dụng: Nén và giải nén tệp tin

## Tổng quan
Lệnh `xz` được sử dụng để nén và giải nén các tệp tin, giúp giảm kích thước tệp tin mà không làm mất dữ liệu. Nó sử dụng thuật toán nén LZMA, mang lại hiệu suất nén cao hơn so với nhiều công cụ nén khác.

## Cách sử dụng
Cú pháp cơ bản của lệnh `xz` như sau:
```
xz [options] [arguments]
```

## Các tùy chọn phổ biến
- `-d`, `--decompress`: Giải nén tệp tin.
- `-k`, `--keep`: Giữ lại tệp tin gốc sau khi nén.
- `-f`, `--force`: Buộc ghi đè lên tệp tin đã tồn tại.
- `-9`: Sử dụng mức nén cao nhất (từ 1 đến 9).
- `-z`: Nén tệp tin (mặc định).

## Ví dụ thường gặp
- Nén một tệp tin:
  ```bash
  xz file.txt
  ```

- Giải nén một tệp tin đã nén:
  ```bash
  xz -d file.txt.xz
  ```

- Nén một tệp tin và giữ lại tệp gốc:
  ```bash
  xz -k file.txt
  ```

- Nén với mức nén cao nhất:
  ```bash
  xz -9 file.txt
  ```

## Mẹo
- Sử dụng tùy chọn `-k` nếu bạn muốn giữ lại tệp gốc sau khi nén.
- Kiểm tra kích thước tệp trước và sau khi nén để đánh giá hiệu quả.
- Nếu bạn cần nén nhiều tệp tin, hãy sử dụng `tar` kết hợp với `xz` để nén cả thư mục:
  ```bash
  tar -cJf archive.tar.xz /path/to/directory
  ```