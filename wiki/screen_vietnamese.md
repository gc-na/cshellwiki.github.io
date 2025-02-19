# [Hệ điều hành] C Shell (csh) screen: Quản lý phiên làm việc

## Tổng quan
Lệnh `screen` trong C Shell (csh) cho phép người dùng tạo và quản lý nhiều phiên làm việc trong một cửa sổ terminal. Nó rất hữu ích cho việc chạy các tác vụ lâu dài mà không cần giữ terminal mở.

## Cách sử dụng
Cú pháp cơ bản của lệnh `screen` như sau:
```
screen [options] [arguments]
```

## Các tùy chọn phổ biến
- `-S <name>`: Đặt tên cho phiên làm việc.
- `-d -r`: Tách rời và khôi phục một phiên làm việc đã tách rời.
- `-list`: Liệt kê tất cả các phiên làm việc hiện có.
- `-L`: Bật ghi lại đầu ra của phiên làm việc vào tệp.

## Ví dụ thường gặp
- **Tạo một phiên mới**:
  ```bash
  screen
  ```

- **Tạo một phiên mới với tên**:
  ```bash
  screen -S mysession
  ```

- **Tách rời phiên làm việc** (sử dụng phím tắt `Ctrl-a d`):
  ```bash
  # Nhấn Ctrl-a sau đó nhấn d
  ```

- **Khôi phục phiên đã tách rời**:
  ```bash
  screen -r mysession
  ```

- **Liệt kê các phiên làm việc**:
  ```bash
  screen -list
  ```

- **Ghi lại đầu ra vào tệp**:
  ```bash
  screen -L
  ```

## Mẹo
- Sử dụng tên phiên để dễ dàng quản lý và khôi phục các phiên làm việc.
- Để thoát khỏi phiên làm việc, bạn có thể sử dụng lệnh `exit` hoặc nhấn `Ctrl-a` sau đó nhấn `k` để kết thúc phiên.
- Thường xuyên kiểm tra các phiên đang chạy để tránh lãng phí tài nguyên hệ thống.