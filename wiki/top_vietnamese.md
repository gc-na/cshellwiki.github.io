# [Linux] Bash top cách sử dụng: Theo dõi tài nguyên hệ thống

## Tổng quan
Lệnh `top` trong Bash được sử dụng để hiển thị thông tin về các tiến trình đang chạy trên hệ thống, bao gồm việc sử dụng CPU, bộ nhớ và các thông số khác. Nó cung cấp một cái nhìn trực quan và thời gian thực về tình trạng của hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `top` như sau:
```
top [options]
```

## Các tùy chọn phổ biến
- `-d <seconds>`: Đặt khoảng thời gian cập nhật (mặc định là 3 giây).
- `-u <username>`: Hiển thị các tiến trình của một người dùng cụ thể.
- `-p <pid>`: Theo dõi một tiến trình cụ thể theo ID tiến trình.
- `-n <number>`: Số lần cập nhật trước khi thoát.

## Ví dụ phổ biến
- Mở lệnh `top` để xem thông tin tiến trình:
  ```bash
  top
  ```

- Cập nhật thông tin mỗi 5 giây:
  ```bash
  top -d 5
  ```

- Hiển thị các tiến trình của người dùng "john":
  ```bash
  top -u john
  ```

- Theo dõi một tiến trình cụ thể với ID là 1234:
  ```bash
  top -p 1234
  ```

- Chạy `top` và chỉ cập nhật 10 lần trước khi thoát:
  ```bash
  top -n 10
  ```

## Mẹo
- Sử dụng phím `h` trong giao diện `top` để xem hướng dẫn sử dụng.
- Nhấn `Shift + M` để sắp xếp các tiến trình theo mức sử dụng bộ nhớ.
- Nhấn `Shift + P` để sắp xếp theo mức sử dụng CPU.
- Bạn có thể nhấn `q` để thoát khỏi giao diện `top` bất cứ lúc nào.