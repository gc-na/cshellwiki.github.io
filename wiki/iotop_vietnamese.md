# [Hệ điều hành] C Shell (csh) iotop: Theo dõi hoạt động I/O của hệ thống

## Tổng quan
Lệnh `iotop` được sử dụng để theo dõi hoạt động I/O (Input/Output) của các tiến trình đang chạy trên hệ thống. Nó giúp người dùng xác định tiến trình nào đang tiêu tốn tài nguyên I/O, từ đó có thể tối ưu hóa hiệu suất hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `iotop` như sau:
```
iotop [tùy chọn] [tham số]
```

## Các tùy chọn phổ biến
- `-o`: Chỉ hiển thị các tiến trình đang sử dụng I/O.
- `-b`: Chạy trong chế độ nền (batch mode), thường được sử dụng để ghi lại dữ liệu.
- `-n <số>`: Chỉ định số lần cập nhật trước khi thoát.
- `-d <giây>`: Đặt khoảng thời gian giữa các lần cập nhật.

## Ví dụ thường gặp
1. **Theo dõi hoạt động I/O theo thời gian thực:**
   ```bash
   iotop
   ```

2. **Chỉ hiển thị các tiến trình đang sử dụng I/O:**
   ```bash
   iotop -o
   ```

3. **Chạy trong chế độ nền và cập nhật 5 lần:**
   ```bash
   iotop -b -n 5
   ```

4. **Đặt khoảng thời gian giữa các lần cập nhật là 2 giây:**
   ```bash
   iotop -d 2
   ```

## Mẹo
- Sử dụng tùy chọn `-o` để chỉ tập trung vào các tiến trình đang hoạt động, giúp giảm bớt thông tin không cần thiết.
- Khi chạy trong chế độ nền, bạn có thể ghi lại kết quả vào một tệp để phân tích sau:
  ```bash
  iotop -b -n 10 > iotop_output.txt
  ```
- Theo dõi thường xuyên hoạt động I/O có thể giúp phát hiện các vấn đề về hiệu suất sớm hơn.