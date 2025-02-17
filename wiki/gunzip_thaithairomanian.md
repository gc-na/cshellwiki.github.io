# [Linux] Bash gunzip sử dụng: Giải nén tệp tin nén

## Overview
Lệnh `gunzip` được sử dụng để giải nén các tệp tin đã được nén bằng thuật toán nén gzip. Lệnh này giúp khôi phục lại các tệp tin về trạng thái ban đầu của chúng, cho phép người dùng truy cập và sử dụng nội dung bên trong.

## Usage
Cú pháp cơ bản của lệnh `gunzip` như sau:
```bash
gunzip [options] [arguments]
```

## Common Options
- `-c`: Giải nén tệp tin và xuất ra stdout mà không xóa tệp gốc.
- `-f`: Buộc giải nén tệp tin, ngay cả khi tệp đã tồn tại.
- `-k`: Giữ lại tệp gốc sau khi giải nén.
- `-r`: Giải nén tệp tin trong thư mục và tất cả các thư mục con.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `gunzip`:

1. Giải nén một tệp tin:
   ```bash
   gunzip file.txt.gz
   ```

2. Giải nén và giữ lại tệp gốc:
   ```bash
   gunzip -k file.txt.gz
   ```

3. Giải nén nhiều tệp tin cùng lúc:
   ```bash
   gunzip file1.gz file2.gz file3.gz
   ```

4. Giải nén tệp tin và xuất ra stdout:
   ```bash
   gunzip -c file.txt.gz > output.txt
   ```

5. Giải nén tất cả tệp tin trong thư mục:
   ```bash
   gunzip *.gz
   ```

## Tips
- Hãy luôn kiểm tra dung lượng ổ đĩa trước khi giải nén để đảm bảo có đủ không gian cho các tệp tin đã giải nén.
- Sử dụng tùy chọn `-k` nếu bạn không muốn mất tệp tin nén gốc.
- Đối với các tệp tin lớn, hãy cân nhắc sử dụng tùy chọn `-c` để xuất ra stdout, giúp bạn dễ dàng kiểm tra nội dung mà không cần lưu lại tệp tin.