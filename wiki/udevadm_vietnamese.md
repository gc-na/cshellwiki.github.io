# [Linux] Bash udevadm Cách sử dụng: Quản lý thiết bị trong hệ thống

## Tổng quan
Lệnh `udevadm` là công cụ quản lý thiết bị trong hệ thống Linux, cho phép người dùng tương tác với hệ thống udev để quản lý và theo dõi các thiết bị phần cứng được kết nối.

## Cách sử dụng
Cú pháp cơ bản của lệnh `udevadm` như sau:
```
udevadm [options] [arguments]
```

## Các tùy chọn phổ biến
- `info`: Hiển thị thông tin về thiết bị.
- `trigger`: Kích hoạt các sự kiện cho thiết bị.
- `settle`: Chờ cho tất cả các sự kiện thiết bị hoàn tất.
- `control`: Quản lý trạng thái của udev daemon.

## Ví dụ phổ biến
1. **Hiển thị thông tin về một thiết bị cụ thể**
   ```bash
   udevadm info --query=all --name=/dev/sda
   ```

2. **Kích hoạt sự kiện cho tất cả các thiết bị**
   ```bash
   udevadm trigger
   ```

3. **Chờ cho tất cả các sự kiện thiết bị hoàn tất**
   ```bash
   udevadm settle
   ```

4. **Quản lý trạng thái của udev daemon**
   ```bash
   udevadm control --reload-rules
   ```

## Mẹo
- Sử dụng `udevadm info` để tìm hiểu chi tiết về các thuộc tính của thiết bị, điều này hữu ích khi bạn cần cấu hình hoặc gỡ lỗi.
- Khi thay đổi quy tắc udev, hãy nhớ sử dụng `udevadm control --reload-rules` để làm mới các quy tắc mà không cần khởi động lại hệ thống.
- Để theo dõi các sự kiện thiết bị trong thời gian thực, bạn có thể sử dụng lệnh `udevadm monitor`.