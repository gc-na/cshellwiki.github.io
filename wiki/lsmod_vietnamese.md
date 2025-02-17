# [Linux] Bash lsmod Cách sử dụng: Hiển thị các mô-đun kernel đang hoạt động

## Tổng quan
Lệnh `lsmod` được sử dụng để hiển thị danh sách các mô-đun kernel hiện đang được tải trong hệ thống Linux. Nó cung cấp thông tin về các mô-đun, bao gồm tên mô-đun, kích thước và số lượng tham chiếu.

## Cách sử dụng
Cú pháp cơ bản của lệnh `lsmod` như sau:

```bash
lsmod [tùy chọn] [tham số]
```

## Các tùy chọn phổ biến
- `-h`, `--help`: Hiển thị thông tin trợ giúp về lệnh `lsmod`.
- `-q`, `--quiet`: Chỉ hiển thị thông tin cần thiết, không có thông báo bổ sung.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `lsmod`:

1. **Hiển thị danh sách tất cả các mô-đun đang hoạt động:**
   ```bash
   lsmod
   ```

2. **Hiển thị thông tin trợ giúp:**
   ```bash
   lsmod --help
   ```

3. **Sử dụng tùy chọn im lặng để chỉ hiển thị thông tin cần thiết:**
   ```bash
   lsmod -q
   ```

## Mẹo
- Sử dụng lệnh `lsmod` để kiểm tra xem các mô-đun cần thiết cho phần cứng của bạn đã được tải hay chưa.
- Kết hợp `lsmod` với lệnh `grep` để tìm kiếm mô-đun cụ thể trong danh sách:
  ```bash
  lsmod | grep <tên_mô-đun>
  ```
- Theo dõi số lượng tham chiếu của các mô-đun để xác định xem chúng có đang được sử dụng hay không, điều này có thể hữu ích khi bạn cần gỡ bỏ mô-đun.