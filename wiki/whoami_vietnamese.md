# [Linux] Bash whoami Cách sử dụng: Xác định người dùng hiện tại

## Tổng quan
Lệnh `whoami` trong Bash được sử dụng để hiển thị tên người dùng hiện tại đang đăng nhập vào hệ thống. Đây là một công cụ hữu ích để xác định danh tính của người dùng trong môi trường dòng lệnh.

## Cách sử dụng
Cú pháp cơ bản của lệnh `whoami` như sau:
```
whoami [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `--help`: Hiển thị thông tin trợ giúp về lệnh `whoami`.
- `--version`: Hiển thị phiên bản của lệnh `whoami`.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `whoami`:

1. Hiển thị tên người dùng hiện tại:
   ```bash
   whoami
   ```

2. Hiển thị thông tin trợ giúp:
   ```bash
   whoami --help
   ```

3. Kiểm tra phiên bản:
   ```bash
   whoami --version
   ```

## Mẹo
- Sử dụng `whoami` trong các script để xác định người dùng đang chạy script đó.
- Kết hợp `whoami` với các lệnh khác để thực hiện các tác vụ dựa trên quyền truy cập của người dùng hiện tại.