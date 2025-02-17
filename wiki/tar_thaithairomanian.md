# [Linux] Bash tar sử dụng: Lưu trữ và nén tệp

## Overview
Lệnh `tar` được sử dụng để lưu trữ và nén các tệp và thư mục trong hệ thống Linux. Nó cho phép người dùng tạo các tệp lưu trữ (archive files) và có thể nén chúng để tiết kiệm không gian lưu trữ.

## Usage
Cú pháp cơ bản của lệnh `tar` như sau:
```bash
tar [options] [arguments]
```

## Common Options
- `-c`: Tạo một tệp lưu trữ mới.
- `-x`: Giải nén tệp lưu trữ.
- `-f`: Chỉ định tên tệp lưu trữ.
- `-v`: Hiển thị thông tin chi tiết trong quá trình thực hiện.
- `-z`: Nén hoặc giải nén tệp bằng gzip.
- `-j`: Nén hoặc giải nén tệp bằng bzip2.

## Common Examples
- Tạo một tệp lưu trữ:
```bash
tar -cvf archive.tar /path/to/directory
```
- Giải nén tệp lưu trữ:
```bash
tar -xvf archive.tar
```
- Tạo tệp lưu trữ nén bằng gzip:
```bash
tar -czvf archive.tar.gz /path/to/directory
```
- Giải nén tệp lưu trữ nén bằng gzip:
```bash
tar -xzvf archive.tar.gz
```

## Tips
- Sử dụng tùy chọn `-v` để theo dõi quá trình thực hiện, giúp bạn biết được tệp nào đang được xử lý.
- Để tiết kiệm không gian, hãy sử dụng tùy chọn nén (`-z` hoặc `-j`) khi tạo tệp lưu trữ.
- Kiểm tra nội dung của tệp lưu trữ mà không cần giải nén bằng cách sử dụng:
```bash
tar -tvf archive.tar
```