# [Linux] Bash gzip Cách sử dụng: Nén và giải nén tệp tin

## Tổng quan
Lệnh `gzip` là một công cụ nén tệp tin trong hệ điều hành Unix và Linux. Nó giúp giảm kích thước tệp tin bằng cách sử dụng thuật toán nén, giúp tiết kiệm không gian lưu trữ và tăng tốc độ truyền tải tệp tin.

## Cách sử dụng
Cú pháp cơ bản của lệnh `gzip` như sau:
```
gzip [tùy chọn] [tệp tin]
```

## Các tùy chọn phổ biến
- `-d`, `--decompress`: Giải nén tệp tin.
- `-k`, `--keep`: Giữ lại tệp tin gốc sau khi nén.
- `-v`, `--verbose`: Hiển thị thông tin chi tiết về quá trình nén.
- `-f`, `--force`: Nén tệp tin ngay cả khi tệp tin đã tồn tại.
- `-r`, `--recursive`: Nén tất cả các tệp tin trong thư mục và các thư mục con.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `gzip`:

1. Nén một tệp tin:
   ```bash
   gzip file.txt
   ```

2. Giải nén một tệp tin đã nén:
   ```bash
   gzip -d file.txt.gz
   ```

3. Nén tệp tin và giữ lại tệp gốc:
   ```bash
   gzip -k file.txt
   ```

4. Nén tất cả tệp tin trong thư mục hiện tại:
   ```bash
   gzip *.txt
   ```

5. Nén một thư mục và tất cả các tệp tin bên trong:
   ```bash
   gzip -r my_directory/
   ```

## Mẹo
- Hãy kiểm tra kích thước tệp tin sau khi nén để đảm bảo rằng quá trình nén đã thành công.
- Sử dụng tùy chọn `-v` để theo dõi tiến trình nén và nhận thông tin chi tiết về kích thước tệp tin trước và sau khi nén.
- Khi nén nhiều tệp tin, hãy cân nhắc sử dụng `tar` kết hợp với `gzip` để tạo một tệp tin nén duy nhất. Ví dụ:
  ```bash
  tar -czf archive.tar.gz my_directory/
  ```