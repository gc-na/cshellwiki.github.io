# [Linux] Bash tar Cách sử dụng: Nén và giải nén tệp tin

## Tổng quan
Lệnh `tar` được sử dụng để nén và giải nén các tệp tin hoặc thư mục trên hệ điều hành Linux. Nó giúp bạn tạo ra các tệp tin lưu trữ (archive) để dễ dàng quản lý và truyền tải.

## Cách sử dụng
Cú pháp cơ bản của lệnh `tar` như sau:
```
tar [options] [arguments]
```

## Các tùy chọn phổ biến
- `-c`: Tạo một tệp tin lưu trữ mới.
- `-x`: Giải nén tệp tin lưu trữ.
- `-f`: Chỉ định tên tệp tin lưu trữ.
- `-v`: Hiển thị thông tin chi tiết trong quá trình thực hiện.
- `-z`: Nén hoặc giải nén tệp tin bằng gzip.
- `-j`: Nén hoặc giải nén tệp tin bằng bzip2.

## Ví dụ phổ biến
1. **Tạo tệp tin lưu trữ**:
   ```bash
   tar -cvf archive.tar /path/to/directory
   ```
   Lệnh này sẽ tạo tệp tin `archive.tar` từ thư mục chỉ định.

2. **Giải nén tệp tin lưu trữ**:
   ```bash
   tar -xvf archive.tar
   ```
   Lệnh này sẽ giải nén nội dung của `archive.tar` vào thư mục hiện tại.

3. **Nén tệp tin bằng gzip**:
   ```bash
   tar -czvf archive.tar.gz /path/to/directory
   ```
   Lệnh này sẽ tạo tệp tin nén `archive.tar.gz` từ thư mục chỉ định.

4. **Giải nén tệp tin nén**:
   ```bash
   tar -xzvf archive.tar.gz
   ```
   Lệnh này sẽ giải nén tệp tin `archive.tar.gz`.

## Mẹo
- Luôn sử dụng tùy chọn `-v` để theo dõi tiến trình khi nén hoặc giải nén.
- Kiểm tra nội dung của tệp tin lưu trữ mà không giải nén bằng lệnh:
  ```bash
  tar -tvf archive.tar
  ```
- Để nén tệp tin với bzip2, thay thế `-z` bằng `-j` trong các lệnh nén.