# [Bash] Bash screen sử dụng: Quản lý nhiều phiên làm việc trong terminal

## Overview
Lệnh `screen` cho phép người dùng quản lý nhiều phiên làm việc trong terminal. Nó giúp bạn tạo và duy trì các phiên làm việc độc lập, cho phép bạn quay lại làm việc mà không bị mất tiến trình.

## Usage
Cú pháp cơ bản của lệnh `screen` như sau:
```bash
screen [options] [arguments]
```

## Common Options
- `-S <session_name>`: Đặt tên cho phiên làm việc.
- `-d -r <session_name>`: Tách rời và khôi phục phiên làm việc đã tách rời.
- `-list`: Liệt kê tất cả các phiên làm việc hiện có.
- `-L`: Bật ghi lại phiên làm việc vào tệp.

## Common Examples
- **Tạo một phiên làm việc mới:**
  ```bash
  screen
  ```
- **Tạo một phiên với tên:**
  ```bash
  screen -S mysession
  ```
- **Liệt kê các phiên làm việc:**
  ```bash
  screen -list
  ```
- **Khôi phục một phiên đã tách rời:**
  ```bash
  screen -d -r mysession
  ```
- **Ghi lại phiên làm việc:**
  ```bash
  screen -L
  ```

## Tips
- Sử dụng phím tắt `Ctrl + A` sau đó nhấn `D` để tách rời phiên mà không đóng nó.
- Để quay lại phiên đã tách rời, sử dụng lệnh `screen -r`.
- Đặt tên cho phiên làm việc giúp dễ dàng quản lý và quay lại các phiên khác nhau.