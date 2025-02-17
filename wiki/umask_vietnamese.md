# [Linux] Bash umask Cách sử dụng: Thiết lập quyền truy cập mặc định cho tệp tin

## Tổng quan
Lệnh `umask` trong Bash được sử dụng để thiết lập quyền truy cập mặc định cho các tệp tin và thư mục mới được tạo ra. Nó xác định các quyền mà sẽ bị từ chối khi tạo tệp hoặc thư mục, giúp bảo vệ dữ liệu của bạn khỏi việc truy cập không mong muốn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `umask` như sau:

```bash
umask [options] [arguments]
```

## Các tùy chọn phổ biến
- `-S`: Hiển thị umask dưới dạng ký hiệu quyền (rwx).
- `-p`: Hiển thị umask hiện tại của shell cha.
- `-c`: Thiết lập umask cho các tệp tin và thư mục mới.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `umask`:

1. **Kiểm tra umask hiện tại:**
   ```bash
   umask
   ```

2. **Thiết lập umask thành 022 (chỉ cho phép quyền ghi cho chủ sở hữu):**
   ```bash
   umask 022
   ```

3. **Hiển thị umask dưới dạng ký hiệu quyền:**
   ```bash
   umask -S
   ```

4. **Thiết lập umask cho phiên làm việc hiện tại:**
   ```bash
   umask 077
   ```

## Mẹo
- Hãy nhớ rằng umask chỉ ảnh hưởng đến các tệp tin và thư mục mới được tạo ra sau khi thiết lập.
- Kiểm tra umask thường xuyên để đảm bảo rằng quyền truy cập của bạn luôn được bảo mật.
- Sử dụng umask trong các script để đảm bảo rằng các tệp tin được tạo ra có quyền truy cập đúng như mong muốn.