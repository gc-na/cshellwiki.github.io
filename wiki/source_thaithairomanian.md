# [Linux] Bash source sử dụng: Chạy tập lệnh trong phiên hiện tại

## Overview
Lệnh `source` trong Bash được sử dụng để thực thi các lệnh trong một tập tin kịch bản trong phiên hiện tại của shell. Điều này có nghĩa là các biến và hàm được định nghĩa trong tập tin sẽ có sẵn ngay lập tức trong phiên làm việc hiện tại.

## Usage
Cú pháp cơ bản của lệnh `source` như sau:
```bash
source [options] [arguments]
```

## Common Options
- `-h`, `--help`: Hiển thị thông tin trợ giúp về lệnh `source`.
- `-V`, `--version`: Hiển thị phiên bản của shell hiện tại.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `source`:

1. **Chạy một tập tin kịch bản**:
   ```bash
   source myscript.sh
   ```

2. **Sử dụng dấu chấm thay cho lệnh source**:
   ```bash
   . myscript.sh
   ```

3. **Tải lại cấu hình của shell**:
   ```bash
   source ~/.bashrc
   ```

4. **Chạy tập tin kịch bản với tham số**:
   ```bash
   source myscript.sh arg1 arg2
   ```

## Tips
- Sử dụng `source` để cập nhật các biến môi trường mà không cần khởi động lại shell.
- Hãy chắc chắn rằng tập tin kịch bản có quyền thực thi nếu bạn muốn chạy nó mà không cần `source`.
- Kiểm tra các lỗi trong tập tin kịch bản trước khi sử dụng `source` để tránh gây ra sự cố trong phiên làm việc của bạn.