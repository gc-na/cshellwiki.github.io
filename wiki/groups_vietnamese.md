# [Linux] Bash groups: Nhóm người dùng trong hệ thống

## Overview
Lệnh `groups` trong Bash được sử dụng để hiển thị các nhóm mà một người dùng thuộc về. Nó giúp người dùng xác định quyền truy cập và các nhóm mà họ có thể tham gia trong hệ thống.

## Usage
Cú pháp cơ bản của lệnh `groups` như sau:
```
groups [options] [arguments]
```

## Common Options
- `-h`, `--help`: Hiển thị thông tin trợ giúp về lệnh.
- `-v`, `--version`: Hiển thị phiên bản của lệnh.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `groups`:

1. **Hiển thị các nhóm của người dùng hiện tại:**
   ```bash
   groups
   ```

2. **Hiển thị các nhóm của một người dùng cụ thể:**
   ```bash
   groups username
   ```

3. **Sử dụng tùy chọn để hiển thị thông tin trợ giúp:**
   ```bash
   groups --help
   ```

## Tips
- Sử dụng lệnh `id` để có thêm thông tin chi tiết về người dùng, bao gồm UID và GID.
- Nếu bạn là quản trị viên, hãy kiểm tra các nhóm của người dùng để đảm bảo rằng họ có quyền truy cập đúng trong hệ thống.
- Lệnh `groups` có thể hữu ích khi bạn cần xác định các quyền truy cập cho các tệp hoặc thư mục cụ thể.