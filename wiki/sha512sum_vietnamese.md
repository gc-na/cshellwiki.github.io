# [Linux] Bash sha512sum Cách sử dụng: Tính toán và xác thực mã băm SHA-512

## Tổng quan
Lệnh `sha512sum` được sử dụng để tính toán và xác thực mã băm SHA-512 cho các tệp. Mã băm SHA-512 là một chuỗi ký tự đại diện cho nội dung của tệp, giúp kiểm tra tính toàn vẹn của dữ liệu.

## Cách sử dụng
Cú pháp cơ bản của lệnh `sha512sum` như sau:
```bash
sha512sum [options] [arguments]
```

## Các tùy chọn phổ biến
- `-b`: Đọc dữ liệu từ tệp nhị phân.
- `-c`: Kiểm tra mã băm từ một tệp danh sách.
- `-h`: Hiển thị thông tin trợ giúp.
- `--quiet`: Không hiển thị thông tin không cần thiết.

## Ví dụ thường gặp
1. **Tính toán mã băm SHA-512 cho một tệp:**
   ```bash
   sha512sum filename.txt
   ```
   Lệnh này sẽ trả về mã băm SHA-512 của tệp `filename.txt`.

2. **Lưu mã băm vào một tệp:**
   ```bash
   sha512sum filename.txt > checksum.txt
   ```
   Mã băm của `filename.txt` sẽ được lưu vào tệp `checksum.txt`.

3. **Kiểm tra mã băm từ một tệp danh sách:**
   ```bash
   sha512sum -c checksum.txt
   ```
   Lệnh này sẽ kiểm tra tính toàn vẹn của các tệp được liệt kê trong `checksum.txt` dựa trên mã băm đã lưu.

4. **Tính toán mã băm cho nhiều tệp:**
   ```bash
   sha512sum file1.txt file2.txt
   ```
   Lệnh này sẽ tính toán mã băm cho cả `file1.txt` và `file2.txt`.

## Mẹo
- Luôn lưu mã băm vào một tệp riêng biệt để dễ dàng kiểm tra sau này.
- Sử dụng tùy chọn `-c` để kiểm tra mã băm thường xuyên, đặc biệt là khi làm việc với dữ liệu quan trọng.
- Đảm bảo rằng bạn sử dụng `sha512sum` trên tệp nhị phân nếu cần thiết để tránh lỗi trong quá trình tính toán.