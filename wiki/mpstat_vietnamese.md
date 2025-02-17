# [Linux] Bash mpstat Cách sử dụng: Theo dõi hiệu suất CPU

## Tổng quan
Lệnh `mpstat` được sử dụng để hiển thị thông tin về hiệu suất CPU trên hệ thống Linux. Nó cung cấp các số liệu thống kê về mức sử dụng CPU theo thời gian, giúp người dùng theo dõi và phân tích hiệu suất của hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `mpstat` như sau:
```
mpstat [options] [arguments]
```

## Các tùy chọn phổ biến
- `-P ALL`: Hiển thị thông tin cho tất cả các CPU.
- `-u`: Hiển thị thông tin sử dụng CPU.
- `-r`: Hiển thị thông tin về bộ nhớ.
- `-h`: Hiển thị thông tin theo định dạng dễ đọc hơn.

## Ví dụ phổ biến
1. Hiển thị thông tin sử dụng CPU cho tất cả các CPU:
   ```bash
   mpstat -P ALL
   ```

2. Hiển thị thông tin sử dụng CPU mỗi giây:
   ```bash
   mpstat 1
   ```

3. Hiển thị thông tin sử dụng CPU và bộ nhớ:
   ```bash
   mpstat -u -r
   ```

4. Hiển thị thông tin sử dụng CPU với định dạng dễ đọc:
   ```bash
   mpstat -h
   ```

## Mẹo
- Sử dụng `mpstat` cùng với `watch` để theo dõi hiệu suất CPU theo thời gian thực:
  ```bash
  watch mpstat 1
  ```
- Kiểm tra thường xuyên hiệu suất CPU để phát hiện sớm các vấn đề về hiệu suất.
- Kết hợp `mpstat` với các công cụ khác như `vmstat` hoặc `iostat` để có cái nhìn tổng quan hơn về hiệu suất hệ thống.