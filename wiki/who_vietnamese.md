# [Linux] Bash who cách sử dụng: Xem danh sách người dùng đang đăng nhập

## Tổng quan
Lệnh `who` trong Bash được sử dụng để hiển thị danh sách những người dùng hiện đang đăng nhập vào hệ thống. Nó cung cấp thông tin về tên người dùng, thời gian đăng nhập, và địa chỉ IP hoặc tên máy của người dùng.

## Cú pháp
Cú pháp cơ bản của lệnh `who` như sau:
```bash
who [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`: Hiển thị tất cả thông tin về người dùng, bao gồm cả thông tin về thời gian và trạng thái.
- `-b`: Hiển thị thời gian khởi động của hệ thống.
- `-q`: Chỉ hiển thị danh sách tên người dùng đang đăng nhập và số lượng người dùng.
- `--help`: Hiển thị thông tin trợ giúp về lệnh `who`.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `who`:

1. Hiển thị danh sách người dùng đang đăng nhập:
   ```bash
   who
   ```

2. Hiển thị thông tin chi tiết về người dùng:
   ```bash
   who -a
   ```

3. Hiển thị thời gian khởi động của hệ thống:
   ```bash
   who -b
   ```

4. Chỉ hiển thị danh sách tên người dùng và số lượng:
   ```bash
   who -q
   ```

## Mẹo
- Sử dụng lệnh `who` kết hợp với `grep` để tìm kiếm thông tin cụ thể về một người dùng:
  ```bash
  who | grep username
  ```
- Thường xuyên kiểm tra danh sách người dùng đăng nhập để phát hiện hoạt động bất thường trên hệ thống.
- Kết hợp lệnh `who` với các lệnh khác như `last` để theo dõi lịch sử đăng nhập của người dùng.