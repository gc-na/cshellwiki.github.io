# [Linux] Bash reboot cách sử dụng: Khởi động lại hệ thống

## Tổng quan
Lệnh `reboot` được sử dụng để khởi động lại hệ thống Linux. Khi lệnh này được thực thi, nó sẽ tắt tất cả các tiến trình đang chạy và khởi động lại máy tính.

## Cú pháp
Cú pháp cơ bản của lệnh `reboot` như sau:
```
reboot [options] [arguments]
```

## Tùy chọn phổ biến
- `-f`: Bỏ qua quá trình tắt máy an toàn và khởi động lại ngay lập tức.
- `-i`: Khởi động lại hệ thống mà không gửi thông báo đến các người dùng đang đăng nhập.
- `-n`: Bỏ qua việc ghi lại hệ thống trước khi khởi động lại.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `reboot`:

1. Khởi động lại hệ thống ngay lập tức:
   ```bash
   reboot
   ```

2. Khởi động lại mà không gửi thông báo đến người dùng:
   ```bash
   reboot -i
   ```

3. Khởi động lại mà bỏ qua quá trình tắt máy an toàn:
   ```bash
   reboot -f
   ```

4. Khởi động lại hệ thống mà không ghi lại:
   ```bash
   reboot -n
   ```

## Mẹo
- Trước khi sử dụng lệnh `reboot`, hãy đảm bảo rằng bạn đã lưu tất cả công việc đang làm để tránh mất dữ liệu.
- Sử dụng tùy chọn `-f` chỉ khi cần thiết, vì nó có thể gây mất dữ liệu nếu có tiến trình đang chạy.
- Nếu bạn đang quản lý một máy chủ từ xa, hãy cân nhắc sử dụng lệnh `shutdown` với tùy chọn khởi động lại để thông báo cho người dùng trước khi khởi động lại.