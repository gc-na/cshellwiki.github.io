# [Hệ điều hành] C Shell (csh) pidstat: Theo dõi thông số sử dụng tài nguyên của tiến trình

## Tổng quan
Lệnh `pidstat` được sử dụng để theo dõi và hiển thị thông tin về việc sử dụng tài nguyên của các tiến trình đang chạy trên hệ thống. Nó cung cấp thông tin chi tiết về CPU, bộ nhớ, và các thông số khác của từng tiến trình.

## Cú pháp
Cú pháp cơ bản của lệnh `pidstat` như sau:
```
pidstat [options] [arguments]
```

## Các tùy chọn thông dụng
- `-h`: Hiển thị tiêu đề cho các cột.
- `-r`: Hiển thị thông tin về việc sử dụng bộ nhớ.
- `-u`: Hiển thị thông tin về việc sử dụng CPU.
- `-p <pid>`: Theo dõi một tiến trình cụ thể bằng cách chỉ định PID.
- `-t`: Hiển thị thông tin cho tất cả các luồng của tiến trình.

## Ví dụ thông dụng
- Theo dõi việc sử dụng CPU của tất cả các tiến trình:
  ```bash
  pidstat -u
  ```

- Theo dõi việc sử dụng bộ nhớ của tất cả các tiến trình:
  ```bash
  pidstat -r
  ```

- Theo dõi một tiến trình cụ thể với PID là 1234:
  ```bash
  pidstat -p 1234
  ```

- Theo dõi việc sử dụng CPU và bộ nhớ của tất cả các luồng trong một tiến trình cụ thể:
  ```bash
  pidstat -t -p 1234
  ```

## Mẹo
- Sử dụng tùy chọn `-h` để có cái nhìn rõ ràng hơn về thông tin hiển thị.
- Kết hợp `pidstat` với các lệnh khác như `grep` để lọc thông tin theo nhu cầu.
- Thực hiện lệnh `pidstat` theo chu kỳ thời gian để theo dõi sự thay đổi trong việc sử dụng tài nguyên.