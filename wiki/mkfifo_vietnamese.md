# [Linux] Bash mkfifo Cách sử dụng: Tạo tệp FIFO

## Overview
Lệnh `mkfifo` trong Bash được sử dụng để tạo ra một tệp FIFO (First In, First Out). Tệp FIFO cho phép truyền dữ liệu giữa các tiến trình một cách đồng bộ, giúp các tiến trình có thể giao tiếp với nhau mà không cần phải sử dụng tệp tạm.

## Usage
Cú pháp cơ bản của lệnh `mkfifo` như sau:
```bash
mkfifo [options] [arguments]
```

## Common Options
- `-m, --mode=MODE`: Đặt quyền truy cập cho tệp FIFO được tạo ra.
- `--help`: Hiển thị thông tin trợ giúp về lệnh.
- `--version`: Hiển thị phiên bản của lệnh `mkfifo`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mkfifo`:

1. **Tạo một tệp FIFO đơn giản:**
   ```bash
   mkfifo myfifo
   ```

2. **Tạo một tệp FIFO với quyền truy cập cụ thể:**
   ```bash
   mkfifo -m 644 myfifo
   ```

3. **Tạo nhiều tệp FIFO cùng lúc:**
   ```bash
   mkfifo fifo1 fifo2 fifo3
   ```

4. **Sử dụng tệp FIFO để truyền dữ liệu giữa hai tiến trình:**
   - Trong một terminal, bạn có thể sử dụng lệnh sau để đọc từ tệp FIFO:
     ```bash
     cat < myfifo
     ```
   - Trong một terminal khác, bạn có thể ghi vào tệp FIFO:
     ```bash
     echo "Hello, FIFO!" > myfifo
     ```

## Tips
- Đảm bảo rằng tệp FIFO đã được tạo ra trước khi cố gắng đọc hoặc ghi vào nó.
- Sử dụng quyền truy cập phù hợp để đảm bảo rằng các tiến trình có thể truy cập tệp FIFO một cách an toàn.
- Bạn có thể sử dụng lệnh `ls -l` để kiểm tra quyền truy cập của tệp FIFO đã tạo.