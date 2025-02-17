# [Linux] Bash kill Cách sử dụng: Kết thúc tiến trình

## Overview
Lệnh `kill` trong Bash được sử dụng để gửi tín hiệu đến một tiến trình, thường là để kết thúc tiến trình đó. Đây là một công cụ hữu ích để quản lý các tiến trình đang chạy trên hệ thống.

## Usage
Cú pháp cơ bản của lệnh `kill` như sau:

```
kill [options] [arguments]
```

## Common Options
- `-l`: Hiển thị danh sách các tín hiệu có thể gửi.
- `-s SIGNAL`: Gửi tín hiệu cụ thể đến tiến trình.
- `-n NUMBER`: Gửi tín hiệu theo số thứ tự.
- `-p`: Chỉ định rằng bạn đang gửi tín hiệu đến một tiến trình cụ thể mà không cần xác nhận.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `kill`:

1. **Kết thúc một tiến trình bằng PID**:
   ```bash
   kill 1234
   ```
   (Trong đó `1234` là ID của tiến trình mà bạn muốn kết thúc.)

2. **Gửi tín hiệu SIGKILL đến một tiến trình**:
   ```bash
   kill -9 1234
   ```
   (Sử dụng `-9` để gửi tín hiệu SIGKILL, buộc tiến trình phải dừng lại ngay lập tức.)

3. **Gửi tín hiệu SIGTERM đến một tiến trình**:
   ```bash
   kill -15 1234
   ```
   (Sử dụng `-15` để gửi tín hiệu SIGTERM, cho phép tiến trình dừng lại một cách an toàn.)

4. **Gửi tín hiệu đến nhiều tiến trình cùng lúc**:
   ```bash
   kill 1234 5678 91011
   ```

5. **Hiển thị danh sách các tín hiệu có thể gửi**:
   ```bash
   kill -l
   ```

## Tips
- Sử dụng `kill -l` để xem danh sách các tín hiệu có thể gửi, giúp bạn chọn tín hiệu phù hợp.
- Trước khi sử dụng `kill -9`, hãy thử sử dụng `kill` mà không có tùy chọn để cho phép tiến trình thực hiện các thao tác dọn dẹp.
- Để tìm PID của một tiến trình, bạn có thể sử dụng lệnh `ps` hoặc `pgrep`. Ví dụ:
  ```bash
  pgrep -f tên_tiến_trình
  ```