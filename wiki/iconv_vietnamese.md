# [Linux] Bash iconv Cách sử dụng: Chuyển đổi mã hóa văn bản

## Tổng quan
Lệnh `iconv` trong Bash được sử dụng để chuyển đổi giữa các định dạng mã hóa văn bản khác nhau. Nó cho phép người dùng chuyển đổi nội dung của tệp từ một mã hóa sang mã hóa khác, giúp đảm bảo tính tương thích và dễ dàng xử lý văn bản.

## Cách sử dụng
Cú pháp cơ bản của lệnh `iconv` như sau:

```bash
iconv [options] [arguments]
```

## Các tùy chọn phổ biến
- `-f, --from-code=CODE`: Chỉ định mã hóa nguồn.
- `-t, --to-code=CODE`: Chỉ định mã hóa đích.
- `-o, --output=FILE`: Ghi kết quả vào tệp đã chỉ định.
- `-c`: Bỏ qua các ký tự không thể chuyển đổi.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `iconv`:

1. Chuyển đổi tệp từ mã hóa UTF-8 sang ISO-8859-1:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
   ```

2. Chuyển đổi tệp từ mã hóa Windows-1252 sang UTF-8:
   ```bash
   iconv -f WINDOWS-1252 -t UTF-8 input.txt -o output.txt
   ```

3. Chuyển đổi đầu ra trực tiếp trên dòng lệnh mà không cần ghi vào tệp:
   ```bash
   iconv -f UTF-8 -t ASCII//TRANSLIT input.txt
   ```

4. Bỏ qua các ký tự không thể chuyển đổi:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 -c input.txt -o output.txt
   ```

## Mẹo
- Luôn kiểm tra mã hóa của tệp nguồn trước khi chuyển đổi để tránh mất dữ liệu.
- Sử dụng tùy chọn `-o` để ghi kết quả vào tệp mới, giúp bảo vệ tệp gốc.
- Nếu không chắc chắn về mã hóa, hãy thử sử dụng lệnh `file` để xác định mã hóa của tệp trước khi chuyển đổi.