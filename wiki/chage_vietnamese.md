# [Hệ điều hành] C Shell (csh) chage <Sử dụng tương đương>: Quản lý thời gian hết hạn mật khẩu người dùng

## Tổng quan
Lệnh `chage` được sử dụng để quản lý các thông tin liên quan đến thời gian hết hạn mật khẩu của người dùng trong hệ thống Unix/Linux. Nó cho phép người quản trị thiết lập và thay đổi các chính sách mật khẩu như thời gian tối thiểu và tối đa giữa các lần thay đổi mật khẩu.

## Cách sử dụng
Cú pháp cơ bản của lệnh `chage` như sau:

```bash
chage [tùy chọn] [tham số]
```

## Các tùy chọn phổ biến
- `-l, --list`: Hiển thị thông tin thời gian hết hạn mật khẩu cho người dùng.
- `-m, --mindays`: Thiết lập số ngày tối thiểu giữa các lần thay đổi mật khẩu.
- `-M, --maxdays`: Thiết lập số ngày tối đa trước khi mật khẩu hết hạn.
- `-I, --inactive`: Thiết lập số ngày không hoạt động trước khi tài khoản bị khóa.
- `-E, --expire`: Thiết lập ngày hết hạn của tài khoản người dùng.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `chage`:

1. Hiển thị thông tin thời gian hết hạn mật khẩu cho người dùng `username`:
   ```bash
   chage -l username
   ```

2. Thiết lập số ngày tối thiểu giữa các lần thay đổi mật khẩu là 7 ngày cho người dùng `username`:
   ```bash
   chage -m 7 username
   ```

3. Thiết lập số ngày tối đa trước khi mật khẩu hết hạn là 90 ngày cho người dùng `username`:
   ```bash
   chage -M 90 username
   ```

4. Thiết lập ngày hết hạn tài khoản cho người dùng `username` vào ngày 31 tháng 12 năm 2023:
   ```bash
   chage -E 2023-12-31 username
   ```

## Mẹo
- Luôn kiểm tra thông tin thời gian hết hạn mật khẩu sau khi thực hiện thay đổi bằng cách sử dụng tùy chọn `-l`.
- Đặt thời gian hết hạn mật khẩu hợp lý để đảm bảo an toàn cho tài khoản mà không gây khó khăn cho người dùng.
- Sử dụng lệnh `chage` cùng với các lệnh khác để tự động hóa quy trình quản lý tài khoản người dùng.