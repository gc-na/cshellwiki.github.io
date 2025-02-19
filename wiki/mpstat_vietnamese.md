# [Hệ điều hành] C Shell (csh) mpstat Cách sử dụng: Theo dõi hiệu suất CPU

## Tổng quan
Lệnh `mpstat` được sử dụng để hiển thị thông tin về hiệu suất của các bộ xử lý trong hệ thống. Nó cho phép người dùng theo dõi mức sử dụng CPU theo thời gian, giúp phát hiện các vấn đề về hiệu suất.

## Cách sử dụng
Cú pháp cơ bản của lệnh `mpstat` như sau:
```
mpstat [options] [arguments]
```

## Các tùy chọn phổ biến
- `-P ALL`: Hiển thị thông tin cho tất cả các CPU.
- `-u`: Hiển thị thông tin về mức sử dụng CPU.
- `-h`: Hiển thị thông tin theo định dạng dễ đọc hơn.
- `interval`: Thời gian giữa các lần cập nhật thông tin (tính bằng giây).
- `count`: Số lần cập nhật thông tin.

## Ví dụ phổ biến
- Hiển thị thông tin sử dụng CPU cho tất cả các bộ xử lý:
  ```bash
  mpstat -P ALL
  ```

- Hiển thị thông tin sử dụng CPU mỗi 2 giây, 5 lần:
  ```bash
  mpstat 2 5
  ```

- Hiển thị thông tin sử dụng CPU với định dạng dễ đọc:
  ```bash
  mpstat -h
  ```

## Mẹo
- Sử dụng tùy chọn `-P ALL` để có cái nhìn tổng quát về tất cả các CPU trong hệ thống.
- Thực hiện lệnh `mpstat` với khoảng thời gian ngắn để theo dõi hiệu suất trong thời gian thực.
- Kết hợp `mpstat` với các lệnh khác như `grep` để lọc thông tin cần thiết.