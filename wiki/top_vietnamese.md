# [Hệ điều hành] C Shell (csh) top: Xem thông tin hệ thống theo thời gian thực

## Tổng quan
Lệnh `top` trong C Shell (csh) được sử dụng để hiển thị thông tin về các tiến trình đang chạy trên hệ thống, bao gồm mức sử dụng CPU, bộ nhớ và nhiều thông tin khác theo thời gian thực. Đây là một công cụ hữu ích để theo dõi hiệu suất hệ thống và quản lý các tiến trình.

## Cách sử dụng
Cú pháp cơ bản của lệnh `top` như sau:
```
top [options] [arguments]
```

## Các tùy chọn phổ biến
- `-d <seconds>`: Đặt khoảng thời gian cập nhật thông tin (mặc định là 3 giây).
- `-u <username>`: Hiển thị chỉ các tiến trình của người dùng cụ thể.
- `-p <pid>`: Theo dõi một tiến trình cụ thể bằng ID tiến trình (PID).

## Ví dụ thường gặp
1. Mở `top` với thông tin mặc định:
   ```csh
   top
   ```

2. Cập nhật thông tin mỗi 5 giây:
   ```csh
   top -d 5
   ```

3. Hiển thị chỉ các tiến trình của người dùng "john":
   ```csh
   top -u john
   ```

4. Theo dõi một tiến trình cụ thể với PID 1234:
   ```csh
   top -p 1234
   ```

## Mẹo
- Sử dụng phím `q` để thoát khỏi giao diện `top` một cách nhanh chóng.
- Bạn có thể sắp xếp các tiến trình theo mức sử dụng CPU hoặc bộ nhớ bằng cách nhấn phím `Shift + M` hoặc `Shift + P`.
- Thường xuyên theo dõi các tiến trình để phát hiện các vấn đề về hiệu suất sớm hơn.