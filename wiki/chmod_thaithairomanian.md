# [Linux] Bash chmod sử dụng: Thay đổi quyền truy cập tệp

## Overview
Lệnh `chmod` được sử dụng để thay đổi quyền truy cập của tệp hoặc thư mục trong hệ thống Unix/Linux. Quyền truy cập này xác định ai có thể đọc, ghi hoặc thực thi tệp.

## Usage
Cú pháp cơ bản của lệnh `chmod` là:

```bash
chmod [options] [arguments]
```

## Common Options
- `-R`: Thay đổi quyền truy cập cho tất cả các tệp và thư mục con trong thư mục được chỉ định.
- `u`: Đại diện cho người sở hữu tệp.
- `g`: Đại diện cho nhóm người dùng.
- `o`: Đại diện cho những người dùng khác.
- `a`: Đại diện cho tất cả mọi người (u, g, o).
- `+`: Thêm quyền.
- `-`: Xóa quyền.
- `=`: Thiết lập quyền cụ thể.

## Common Examples
- **Thêm quyền thực thi cho người sở hữu tệp:**
  ```bash
  chmod u+x filename
  ```

- **Xóa quyền ghi cho nhóm:**
  ```bash
  chmod g-w filename
  ```

- **Thiết lập quyền đọc cho tất cả mọi người:**
  ```bash
  chmod a+r filename
  ```

- **Thay đổi quyền cho tất cả các tệp và thư mục con trong thư mục:**
  ```bash
  chmod -R 755 directoryname
  ```

## Tips
- Sử dụng `ls -l` để kiểm tra quyền truy cập hiện tại của tệp trước khi thay đổi.
- Hãy cẩn thận khi sử dụng tùy chọn `-R`, vì nó sẽ áp dụng thay đổi cho tất cả các tệp và thư mục con.
- Đảm bảo bạn có quyền cần thiết để thay đổi quyền truy cập của tệp hoặc thư mục.