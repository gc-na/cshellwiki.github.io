# [Linux] Bash shutdown lệnh: Tắt máy tính hoặc khởi động lại hệ thống

## Tổng quan
Lệnh `shutdown` trong Bash được sử dụng để tắt máy tính hoặc khởi động lại hệ thống một cách an toàn. Nó cho phép người dùng lên lịch tắt máy hoặc khởi động lại, giúp đảm bảo rằng tất cả các tiến trình đang chạy được xử lý đúng cách trước khi hệ thống tắt.

## Cú pháp
Cú pháp cơ bản của lệnh `shutdown` như sau:
```
shutdown [options] [time] [message]
```

## Các tùy chọn phổ biến
- `-h` hoặc `--halt`: Tắt máy tính ngay lập tức.
- `-r` hoặc `--reboot`: Khởi động lại máy tính.
- `-P` hoặc `--poweroff`: Tắt máy tính và ngắt nguồn.
- `now`: Thực hiện lệnh ngay lập tức.
- `+m`: Tắt máy sau `m` phút (ví dụ: `+5` để tắt sau 5 phút).
- `hh:mm`: Đặt thời gian tắt máy theo định dạng giờ:phút.

## Ví dụ phổ biến
- Tắt máy ngay lập tức:
  ```bash
  shutdown now
  ```

- Khởi động lại máy tính ngay lập tức:
  ```bash
  shutdown -r now
  ```

- Tắt máy sau 10 phút:
  ```bash
  shutdown +10
  ```

- Tắt máy vào lúc 22:30:
  ```bash
  shutdown 22:30
  ```

- Gửi thông báo trước khi tắt máy:
  ```bash
  shutdown -h +5 "Máy tính sẽ tắt sau 5 phút. Vui lòng lưu công việc của bạn."
  ```

## Mẹo
- Luôn thông báo cho người dùng khác trước khi tắt máy để họ có thể lưu công việc của mình.
- Sử dụng tùy chọn `-r` để khởi động lại máy tính nếu bạn cần áp dụng các thay đổi cấu hình mà không cần tắt nguồn hoàn toàn.
- Kiểm tra các tiến trình đang chạy trước khi tắt máy để tránh mất dữ liệu.