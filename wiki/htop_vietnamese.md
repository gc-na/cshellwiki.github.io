# [Linux] Bash htop Cách sử dụng: Quản lý tiến trình hệ thống

## Tổng quan
Lệnh `htop` là một công cụ tương tác để theo dõi và quản lý các tiến trình đang chạy trên hệ thống. Nó cung cấp một giao diện người dùng trực quan hơn so với lệnh `top`, cho phép người dùng dễ dàng xem thông tin về CPU, bộ nhớ, và các tiến trình khác.

## Cách sử dụng
Cú pháp cơ bản của lệnh `htop` như sau:

```bash
htop [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-h`, `--help`: Hiển thị thông tin trợ giúp về lệnh htop.
- `-s`, `--sort`: Sắp xếp các tiến trình theo một tiêu chí nhất định (ví dụ: CPU, bộ nhớ).
- `-p`, `--pid`: Chỉ hiển thị thông tin cho một hoặc nhiều PID cụ thể.
- `-C`, `--no-color`: Chạy htop mà không có màu sắc.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `htop`:

1. Mở htop để xem các tiến trình đang chạy:
   ```bash
   htop
   ```

2. Mở htop và sắp xếp theo mức sử dụng CPU:
   ```bash
   htop -s PERCENT_CPU
   ```

3. Chỉ hiển thị thông tin cho một PID cụ thể (ví dụ PID 1234):
   ```bash
   htop -p 1234
   ```

4. Mở htop mà không có màu sắc:
   ```bash
   htop -C
   ```

## Mẹo
- Sử dụng phím mũi tên để điều hướng giữa các tiến trình và phím F9 để gửi tín hiệu đến tiến trình (ví dụ: dừng hoặc kết thúc).
- Bạn có thể tìm kiếm tiến trình bằng cách nhấn `F3` và nhập tên tiến trình.
- Để tùy chỉnh cách hiển thị, nhấn `F2` để truy cập vào menu cấu hình.