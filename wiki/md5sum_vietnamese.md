# [Linux] Bash md5sum: Tính toán và kiểm tra giá trị MD5

## Tổng quan
Lệnh `md5sum` được sử dụng để tính toán và kiểm tra giá trị băm MD5 của một tệp tin hoặc chuỗi dữ liệu. Giá trị băm MD5 là một chuỗi 128-bit được biểu diễn dưới dạng 32 ký tự thập lục phân, thường được sử dụng để xác minh tính toàn vẹn của dữ liệu.

## Cú pháp
Cú pháp cơ bản của lệnh `md5sum` như sau:
```
md5sum [options] [arguments]
```

## Các tùy chọn phổ biến
- `-b`: Xử lý tệp nhị phân.
- `-c`: Kiểm tra giá trị băm từ một tệp chứa các giá trị băm.
- `-t`: Tính toán giá trị băm cho dữ liệu từ stdin.
- `--help`: Hiển thị thông tin trợ giúp về lệnh.

## Ví dụ phổ biến
1. **Tính toán giá trị băm MD5 cho một tệp tin:**
   ```bash
   md5sum example.txt
   ```

2. **Lưu giá trị băm vào một tệp tin:**
   ```bash
   md5sum example.txt > checksum.md5
   ```

3. **Kiểm tra giá trị băm từ tệp chứa giá trị băm:**
   ```bash
   md5sum -c checksum.md5
   ```

4. **Tính toán giá trị băm cho dữ liệu nhập từ stdin:**
   ```bash
   echo "Hello, World!" | md5sum
   ```

## Mẹo
- Luôn kiểm tra giá trị băm của tệp tin tải về để đảm bảo tính toàn vẹn của dữ liệu.
- Sử dụng tùy chọn `-b` khi làm việc với tệp nhị phân để tránh lỗi trong quá trình tính toán.
- Lưu trữ giá trị băm trong một tệp tin để dễ dàng kiểm tra sau này.