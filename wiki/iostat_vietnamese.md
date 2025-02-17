# [Linux] Bash iostat Cách sử dụng: Theo dõi hiệu suất I/O

## Tổng quan
Lệnh `iostat` được sử dụng để theo dõi hiệu suất của các thiết bị lưu trữ và hệ thống. Nó cung cấp thông tin về mức sử dụng CPU và hoạt động I/O của các thiết bị, giúp người dùng phân tích hiệu suất hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `iostat` như sau:
```bash
iostat [options] [arguments]
```

## Các tùy chọn phổ biến
- `-c`: Hiển thị thông tin về CPU.
- `-d`: Hiển thị thông tin về các thiết bị lưu trữ.
- `-x`: Hiển thị thông tin chi tiết về các thiết bị.
- `-t`: Hiển thị thời gian thực.
- `interval`: Khoảng thời gian giữa các lần báo cáo.
- `count`: Số lần báo cáo.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `iostat`:

1. Hiển thị thông tin CPU:
   ```bash
   iostat -c
   ```

2. Hiển thị thông tin về các thiết bị lưu trữ:
   ```bash
   iostat -d
   ```

3. Hiển thị thông tin chi tiết về các thiết bị với khoảng thời gian 2 giây, báo cáo 5 lần:
   ```bash
   iostat -x 2 5
   ```

4. Hiển thị thông tin CPU và thiết bị cùng một lúc:
   ```bash
   iostat -c -d
   ```

## Mẹo
- Sử dụng tùy chọn `-t` để thêm thời gian vào báo cáo, giúp bạn theo dõi hiệu suất theo thời gian.
- Kết hợp với lệnh `grep` để lọc thông tin cụ thể mà bạn cần.
- Thực hiện lệnh `iostat` với quyền root để có thông tin chi tiết hơn về các thiết bị.