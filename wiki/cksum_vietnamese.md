# [Linux] Bash cksum: Tính toán giá trị kiểm tra của tệp

## Overview
Lệnh `cksum` trong Bash được sử dụng để tính toán và hiển thị giá trị kiểm tra (checksum) của một tệp. Giá trị kiểm tra này giúp xác định tính toàn vẹn của tệp, cho phép người dùng phát hiện các thay đổi hoặc lỗi trong dữ liệu.

## Usage
Cú pháp cơ bản của lệnh `cksum` như sau:

```bash
cksum [options] [arguments]
```

## Common Options
- `-a, --algorithm=ALGORITHM`: Chọn thuật toán để tính toán giá trị kiểm tra.
- `-h, --help`: Hiển thị thông tin trợ giúp về lệnh `cksum`.
- `-V, --version`: Hiển thị thông tin phiên bản của lệnh `cksum`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `cksum`:

1. Tính toán giá trị kiểm tra của một tệp đơn giản:
   ```bash
   cksum filename.txt
   ```

2. Tính toán giá trị kiểm tra cho nhiều tệp:
   ```bash
   cksum file1.txt file2.txt file3.txt
   ```

3. Sử dụng tùy chọn `-a` để chỉ định thuật toán:
   ```bash
   cksum -a md5 filename.txt
   ```

4. Hiển thị thông tin trợ giúp:
   ```bash
   cksum --help
   ```

## Tips
- Hãy luôn kiểm tra giá trị kiểm tra của tệp sau khi tải xuống từ Internet để đảm bảo tính toàn vẹn.
- Sử dụng `cksum` trong các kịch bản tự động để theo dõi sự thay đổi của tệp theo thời gian.
- Kết hợp `cksum` với các lệnh khác như `find` để kiểm tra nhiều tệp trong một thư mục.