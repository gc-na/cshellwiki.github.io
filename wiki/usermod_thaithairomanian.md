# [Linux] Bash usermod sử dụng: Quản lý người dùng trong hệ thống

## Overview
Lệnh `usermod` trong Bash được sử dụng để thay đổi các thuộc tính của người dùng đã tồn tại trong hệ thống. Bạn có thể sử dụng lệnh này để cập nhật thông tin như tên người dùng, nhóm người dùng, và nhiều thuộc tính khác.

## Usage
Cú pháp cơ bản của lệnh `usermod` là:

```bash
usermod [options] [arguments]
```

## Common Options
- `-aG` : Thêm người dùng vào nhóm mà không xóa khỏi các nhóm khác.
- `-d` : Thay đổi thư mục home của người dùng.
- `-l` : Đổi tên người dùng.
- `-s` : Thay đổi shell đăng nhập của người dùng.
- `-u` : Thay đổi UID của người dùng.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `usermod`:

1. **Thêm người dùng vào nhóm**:
   ```bash
   usermod -aG sudo username
   ```

2. **Đổi tên người dùng**:
   ```bash
   usermod -l newusername oldusername
   ```

3. **Thay đổi thư mục home**:
   ```bash
   usermod -d /new/home/path username
   ```

4. **Thay đổi shell đăng nhập**:
   ```bash
   usermod -s /bin/zsh username
   ```

5. **Thay đổi UID của người dùng**:
   ```bash
   usermod -u 1001 username
   ```

## Tips
- Luôn sao lưu dữ liệu quan trọng trước khi thực hiện bất kỳ thay đổi nào đối với người dùng.
- Sử dụng tùy chọn `-aG` khi thêm người dùng vào nhóm để đảm bảo họ không bị xóa khỏi các nhóm khác.
- Kiểm tra các thay đổi bằng cách sử dụng lệnh `id username` sau khi thực hiện `usermod` để xác nhận các thuộc tính mới.