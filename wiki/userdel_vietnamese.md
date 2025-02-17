# [Linux] Bash userdel cách sử dụng: Xóa người dùng trong hệ thống

## Tổng quan
Lệnh `userdel` được sử dụng để xóa một tài khoản người dùng khỏi hệ thống Linux. Khi tài khoản người dùng bị xóa, tất cả các tệp tin và thư mục thuộc về người dùng đó có thể cũng sẽ bị xóa, tùy thuộc vào các tùy chọn được sử dụng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `userdel` như sau:

```bash
userdel [options] [username]
```

## Các tùy chọn phổ biến
- `-r`: Xóa thư mục chính của người dùng và tất cả các tệp tin bên trong.
- `-f`: Buộc xóa tài khoản người dùng ngay cả khi người dùng đang đăng nhập.
- `-Z`: Xóa nhãn SELinux của người dùng.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `userdel`:

1. **Xóa một người dùng mà không xóa thư mục chính:**
   ```bash
   userdel username
   ```

2. **Xóa một người dùng và thư mục chính của họ:**
   ```bash
   userdel -r username
   ```

3. **Buộc xóa một người dùng đang đăng nhập:**
   ```bash
   userdel -f username
   ```

4. **Xóa một người dùng và nhãn SELinux của họ:**
   ```bash
   userdel -Z username
   ```

## Mẹo
- Trước khi xóa một tài khoản người dùng, hãy đảm bảo rằng bạn đã sao lưu tất cả các tệp tin quan trọng của họ.
- Kiểm tra xem người dùng có đang đăng nhập hay không bằng lệnh `who` trước khi sử dụng tùy chọn `-f`.
- Sử dụng lệnh `cat /etc/passwd` để xác nhận tên người dùng trước khi xóa.