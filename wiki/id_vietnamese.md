# [Linux] Bash id cách sử dụng: Xem thông tin người dùng

## Overview
Lệnh `id` trong Bash được sử dụng để hiển thị thông tin về người dùng hiện tại hoặc một người dùng cụ thể. Thông tin này bao gồm UID (User ID), GID (Group ID) và các nhóm mà người dùng thuộc về.

## Usage
Cú pháp cơ bản của lệnh `id` như sau:
```
id [options] [arguments]
```

## Common Options
- `-u`: Hiển thị UID của người dùng.
- `-g`: Hiển thị GID của nhóm chính.
- `-G`: Hiển thị tất cả các GID mà người dùng thuộc về.
- `-n`: Hiển thị tên thay vì ID.
- `-r`: Hiển thị ID thực tế (real ID) thay vì ID hiệu lực (effective ID).

## Common Examples
- Hiển thị thông tin của người dùng hiện tại:
  ```bash
  id
  ```

- Hiển thị UID của người dùng hiện tại:
  ```bash
  id -u
  ```

- Hiển thị GID của nhóm chính:
  ```bash
  id -g
  ```

- Hiển thị tất cả các GID mà người dùng thuộc về:
  ```bash
  id -G
  ```

- Hiển thị thông tin của một người dùng cụ thể (ví dụ: `username`):
  ```bash
  id username
  ```

- Hiển thị tên người dùng thay vì UID:
  ```bash
  id -n -u
  ```

## Tips
- Sử dụng lệnh `id` mà không có tham số để nhanh chóng kiểm tra thông tin người dùng hiện tại.
- Kết hợp các tùy chọn để có được thông tin chi tiết hơn, chẳng hạn như `id -nG` để hiển thị tên của tất cả các nhóm mà người dùng thuộc về.
- Lệnh `id` rất hữu ích trong việc kiểm tra quyền truy cập và xác định các nhóm mà người dùng có thể tham gia.