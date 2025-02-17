# [Linux] Bash id sử dụng: Xem thông tin người dùng

## Overview
Lệnh `id` trong Bash được sử dụng để hiển thị thông tin về người dùng hiện tại hoặc một người dùng cụ thể. Nó cung cấp các chi tiết như UID (User ID), GID (Group ID), và các nhóm mà người dùng đó thuộc về.

## Usage
Cú pháp cơ bản của lệnh `id` như sau:
```
id [options] [arguments]
```

## Common Options
- `-u`: Hiển thị UID của người dùng.
- `-g`: Hiển thị GID của nhóm chính.
- `-G`: Hiển thị tất cả các GID mà người dùng thuộc về.
- `-n`: Hiển thị tên thay vì số cho UID hoặc GID.
- `-r`: Hiển thị GID của nhóm chính mà không có thông tin nhóm.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `id`:

1. Hiển thị thông tin của người dùng hiện tại:
   ```bash
   id
   ```

2. Hiển thị UID của người dùng hiện tại:
   ```bash
   id -u
   ```

3. Hiển thị GID của nhóm chính:
   ```bash
   id -g
   ```

4. Hiển thị tất cả các GID mà người dùng thuộc về:
   ```bash
   id -G
   ```

5. Hiển thị thông tin của một người dùng cụ thể (ví dụ: user1):
   ```bash
   id user1
   ```

## Tips
- Sử dụng `id -n` để dễ dàng đọc tên thay vì số cho UID hoặc GID.
- Kết hợp với các lệnh khác như `grep` để lọc thông tin cụ thể từ đầu ra của `id`.
- Thường xuyên kiểm tra thông tin người dùng và nhóm để đảm bảo quyền truy cập chính xác trong các dự án hợp tác.