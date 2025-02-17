# [Linux] Bash chage Cách sử dụng: Quản lý thời gian hết hạn mật khẩu người dùng

## Overview
Lệnh `chage` được sử dụng để quản lý thời gian hết hạn mật khẩu cho người dùng trong hệ thống Linux. Nó cho phép bạn thiết lập và điều chỉnh các thông số liên quan đến mật khẩu, như thời gian tối thiểu và tối đa giữa các lần thay đổi mật khẩu.

## Usage
Cú pháp cơ bản của lệnh `chage` như sau:
```bash
chage [options] [arguments]
```

## Common Options
- `-l, --list`: Hiển thị thông tin về thời gian hết hạn mật khẩu của người dùng.
- `-m, --mindays`: Thiết lập số ngày tối thiểu giữa các lần thay đổi mật khẩu.
- `-M, --maxdays`: Thiết lập số ngày tối đa mà mật khẩu có thể sử dụng trước khi hết hạn.
- `-I, --inactive`: Thiết lập số ngày không hoạt động trước khi tài khoản bị khóa.
- `-E, --expire`: Thiết lập ngày hết hạn cho tài khoản người dùng.

## Common Examples
1. **Hiển thị thông tin về thời gian hết hạn mật khẩu của người dùng:**
   ```bash
   chage -l username
   ```

2. **Thiết lập số ngày tối thiểu giữa các lần thay đổi mật khẩu là 7 ngày:**
   ```bash
   chage -m 7 username
   ```

3. **Thiết lập số ngày tối đa mà mật khẩu có thể sử dụng là 30 ngày:**
   ```bash
   chage -M 30 username
   ```

4. **Thiết lập số ngày không hoạt động trước khi tài khoản bị khóa là 15 ngày:**
   ```bash
   chage -I 15 username
   ```

5. **Thiết lập ngày hết hạn cho tài khoản người dùng:**
   ```bash
   chage -E 2024-12-31 username
   ```

## Tips
- Luôn kiểm tra thông tin mật khẩu của người dùng sau khi thực hiện thay đổi bằng lệnh `chage -l username`.
- Đặt các giá trị hợp lý cho thời gian hết hạn mật khẩu để bảo mật tốt hơn mà không làm phiền người dùng quá nhiều.
- Sử dụng lệnh `chage` với quyền root hoặc sudo để đảm bảo bạn có quyền thay đổi thông tin của người dùng.