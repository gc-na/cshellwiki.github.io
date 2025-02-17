# [Linux] Bash iotop Cách sử dụng: Theo dõi hoạt động I/O của hệ thống

## Tổng quan
Lệnh `iotop` là một công cụ mạnh mẽ trong Bash giúp theo dõi và hiển thị hoạt động I/O (Input/Output) của các tiến trình đang chạy trên hệ thống. Nó cho phép người dùng xem các tiến trình nào đang tiêu tốn băng thông đĩa, từ đó giúp chẩn đoán các vấn đề liên quan đến hiệu suất.

## Cách sử dụng
Cú pháp cơ bản của lệnh `iotop` như sau:
```bash
iotop [options] [arguments]
```

## Các tùy chọn phổ biến
- `-o`, `--only`: Chỉ hiển thị các tiến trình đang sử dụng I/O.
- `-b`, `--batch`: Chạy trong chế độ batch, phù hợp cho việc ghi lại dữ liệu.
- `-n NUM`, `--iter NUM`: Chỉ định số lần cập nhật trước khi thoát.
- `-d SEC`, `--delay SEC`: Đặt thời gian chờ giữa các lần cập nhật.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế khi sử dụng `iotop`:

1. **Chạy iotop để theo dõi I/O của tất cả các tiến trình:**
   ```bash
   iotop
   ```

2. **Chỉ hiển thị các tiến trình đang sử dụng I/O:**
   ```bash
   iotop -o
   ```

3. **Chạy iotop trong chế độ batch với 5 lần cập nhật:**
   ```bash
   iotop -b -n 5
   ```

4. **Đặt thời gian chờ giữa các lần cập nhật là 2 giây:**
   ```bash
   iotop -d 2
   ```

## Mẹo
- Sử dụng tùy chọn `-o` để nhanh chóng xác định các tiến trình đang gây ra tải I/O cao.
- Chạy `iotop` với quyền root để có thể xem tất cả các tiến trình, bao gồm cả những tiến trình của người dùng khác.
- Kết hợp `iotop` với các công cụ giám sát khác như `htop` để có cái nhìn tổng quan hơn về hiệu suất hệ thống.