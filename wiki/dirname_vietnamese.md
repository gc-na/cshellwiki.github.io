# [Linux] Bash dirname cách sử dụng: Lấy tên thư mục chứa tệp

## Overview
Lệnh `dirname` trong Bash được sử dụng để trích xuất tên thư mục chứa một tệp hoặc đường dẫn. Nó giúp người dùng dễ dàng lấy phần thư mục của một đường dẫn mà không cần phải xử lý thủ công.

## Usage
Cú pháp cơ bản của lệnh `dirname` như sau:

```bash
dirname [options] [arguments]
```

## Common Options
- `-z`, `--zero`: Kết thúc mỗi tên đường dẫn bằng ký tự null, hữu ích khi xử lý các tên đường dẫn có khoảng trắng.
- `--help`: Hiển thị thông tin trợ giúp về lệnh `dirname`.
- `--version`: Hiển thị phiên bản của lệnh `dirname`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `dirname`:

1. **Lấy tên thư mục từ đường dẫn tệp:**
   ```bash
   dirname /home/user/documents/file.txt
   ```
   Kết quả: `/home/user/documents`

2. **Lấy tên thư mục từ đường dẫn tương đối:**
   ```bash
   dirname ./projects/script.sh
   ```
   Kết quả: `./projects`

3. **Làm việc với nhiều đường dẫn:**
   ```bash
   dirname /var/log/syslog /etc/hosts
   ```
   Kết quả:
   ```
   /var/log
   /etc
   ```

4. **Sử dụng với ký tự null:**
   ```bash
   printf "/home/user/documents/file.txt\0" | xargs -0 dirname
   ```
   Kết quả: `/home/user/documents`

## Tips
- Sử dụng `dirname` trong các kịch bản tự động hóa để dễ dàng quản lý và thao tác với đường dẫn tệp.
- Kết hợp `dirname` với các lệnh khác như `basename` để xử lý đường dẫn một cách hiệu quả hơn.
- Hãy nhớ kiểm tra các tùy chọn của lệnh bằng cách sử dụng `dirname --help` để biết thêm chi tiết.