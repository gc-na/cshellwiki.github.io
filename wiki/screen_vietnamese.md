# [Linux] Bash screen cách sử dụng: Quản lý phiên làm việc trong terminal

## Tổng quan
Lệnh `screen` cho phép người dùng tạo và quản lý nhiều phiên làm việc trong terminal. Nó rất hữu ích khi bạn muốn chạy các tác vụ lâu dài mà không cần phải giữ terminal mở liên tục.

## Cách sử dụng
Cú pháp cơ bản của lệnh `screen` như sau:
```
screen [options] [arguments]
```

## Tùy chọn phổ biến
- `-S <name>`: Đặt tên cho phiên làm việc mới.
- `-d -r <name>`: Ngắt kết nối và kết nối lại với phiên đã tồn tại.
- `-list`: Liệt kê tất cả các phiên `screen` đang hoạt động.
- `-h <lines>`: Thiết lập số dòng lịch sử mà `screen` sẽ lưu.

## Ví dụ phổ biến
1. **Tạo một phiên mới**:
   ```bash
   screen
   ```

2. **Tạo một phiên mới với tên**:
   ```bash
   screen -S mysession
   ```

3. **Liệt kê các phiên đang chạy**:
   ```bash
   screen -list
   ```

4. **Ngắt kết nối khỏi phiên**:
   Nhấn `Ctrl + A`, sau đó nhấn `D`.

5. **Kết nối lại với phiên đã ngắt**:
   ```bash
   screen -r mysession
   ```

## Mẹo
- Sử dụng tên cho các phiên làm việc để dễ dàng quản lý và nhận diện.
- Thường xuyên lưu lại công việc của bạn trong các phiên `screen` để tránh mất dữ liệu.
- Nếu bạn cần chạy một lệnh lâu dài, hãy sử dụng `screen` để đảm bảo rằng nó tiếp tục chạy ngay cả khi bạn ngắt kết nối.