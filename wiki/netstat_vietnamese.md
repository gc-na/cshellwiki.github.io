# [Hệ điều hành] C Shell (csh) netstat Cách sử dụng: Hiển thị thông tin mạng

## Tổng quan
Lệnh `netstat` được sử dụng để hiển thị các kết nối mạng, bảng định tuyến, và các thông tin khác liên quan đến mạng trên hệ thống. Nó rất hữu ích để theo dõi trạng thái mạng và phát hiện các vấn đề liên quan đến kết nối.

## Cách sử dụng
Cú pháp cơ bản của lệnh `netstat` như sau:
```
netstat [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`: Hiển thị tất cả các kết nối và cổng đang lắng nghe.
- `-n`: Hiển thị địa chỉ IP và số cổng thay vì tên miền.
- `-t`: Hiển thị các kết nối TCP.
- `-u`: Hiển thị các kết nối UDP.
- `-r`: Hiển thị bảng định tuyến.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `netstat`:

1. Hiển thị tất cả các kết nối và cổng đang lắng nghe:
   ```csh
   netstat -a
   ```

2. Hiển thị các kết nối TCP:
   ```csh
   netstat -t
   ```

3. Hiển thị địa chỉ IP và số cổng thay vì tên miền:
   ```csh
   netstat -n
   ```

4. Hiển thị bảng định tuyến:
   ```csh
   netstat -r
   ```

5. Hiển thị các kết nối UDP:
   ```csh
   netstat -u
   ```

## Mẹo
- Sử dụng tùy chọn `-n` để tăng tốc độ hiển thị, đặc biệt khi có nhiều kết nối.
- Kết hợp các tùy chọn để có được thông tin chi tiết hơn, ví dụ: `netstat -an` để xem tất cả các kết nối với địa chỉ IP.
- Thường xuyên kiểm tra trạng thái mạng của bạn để phát hiện sớm các vấn đề tiềm ẩn.