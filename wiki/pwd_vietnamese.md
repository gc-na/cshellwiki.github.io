# [Linux] Bash pwd cách sử dụng: Lấy đường dẫn thư mục hiện tại

## Overview
Lệnh `pwd` (print working directory) được sử dụng để hiển thị đường dẫn tuyệt đối của thư mục hiện tại mà bạn đang làm việc trong terminal. Đây là một lệnh cơ bản nhưng rất hữu ích trong việc xác định vị trí của bạn trong hệ thống tệp.

## Usage
Cú pháp cơ bản của lệnh `pwd` như sau:
```
pwd [options] [arguments]
```

## Common Options
- `-L`: Hiển thị đường dẫn logic (theo liên kết mềm).
- `-P`: Hiển thị đường dẫn vật lý (theo liên kết cứng).

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `pwd`:

1. **Hiển thị đường dẫn hiện tại**:
   ```bash
   pwd
   ```

2. **Hiển thị đường dẫn vật lý**:
   ```bash
   pwd -P
   ```

3. **Hiển thị đường dẫn logic**:
   ```bash
   pwd -L
   ```

## Tips
- Sử dụng `pwd` thường xuyên để xác định vị trí của bạn trong hệ thống tệp, đặc biệt khi làm việc với nhiều thư mục.
- Kết hợp `pwd` với các lệnh khác như `cd` để dễ dàng điều hướng trong terminal.
- Nếu bạn đang viết script, hãy sử dụng `pwd` để lấy đường dẫn hiện tại và lưu nó vào biến để sử dụng sau này.