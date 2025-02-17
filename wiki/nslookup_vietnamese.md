# [Linux] Bash nslookup Cách sử dụng: Tra cứu thông tin DNS

## Tổng quan
Lệnh `nslookup` được sử dụng để truy vấn thông tin về tên miền và địa chỉ IP từ hệ thống DNS (Domain Name System). Nó cho phép người dùng kiểm tra và xác minh các bản ghi DNS, giúp xác định các vấn đề liên quan đến mạng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `nslookup` như sau:

```bash
nslookup [options] [arguments]
```

## Các tùy chọn phổ biến
- `-type=TYPE`: Chỉ định loại bản ghi DNS cần truy vấn, ví dụ như A, AAAA, MX, TXT.
- `-timeout=SECONDS`: Đặt thời gian chờ cho mỗi truy vấn.
- `-retry=COUNT`: Đặt số lần thử lại khi không nhận được phản hồi.
- `-debug`: Hiển thị thông tin chi tiết về quá trình truy vấn.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `nslookup`:

1. Tra cứu địa chỉ IP của một tên miền:
   ```bash
   nslookup example.com
   ```

2. Tra cứu bản ghi MX (Mail Exchange) của một tên miền:
   ```bash
   nslookup -type=MX example.com
   ```

3. Tra cứu bản ghi TXT của một tên miền:
   ```bash
   nslookup -type=TXT example.com
   ```

4. Sử dụng một máy chủ DNS cụ thể để thực hiện truy vấn:
   ```bash
   nslookup example.com 8.8.8.8
   ```

## Mẹo
- Sử dụng tùy chọn `-debug` để nhận thêm thông tin chi tiết khi gặp vấn đề với truy vấn DNS.
- Kiểm tra nhiều loại bản ghi khác nhau để có cái nhìn toàn diện về cấu hình DNS của tên miền.
- Lưu ý rằng một số tên miền có thể có nhiều bản ghi, vì vậy hãy xem xét tất cả các kết quả trả về.