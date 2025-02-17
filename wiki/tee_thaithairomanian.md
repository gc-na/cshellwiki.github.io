# [Linux] Bash tee sử dụng: Ghi và hiển thị đầu ra

## Overview
Lệnh `tee` trong Bash được sử dụng để đọc từ đầu vào chuẩn và ghi vào cả đầu ra chuẩn và một hoặc nhiều tệp. Điều này cho phép bạn xem dữ liệu trong khi cũng lưu trữ nó cho các mục đích sử dụng sau.

## Usage
Cú pháp cơ bản của lệnh `tee` là:

```bash
tee [options] [arguments]
```

## Common Options
- `-a`, `--append`: Thêm đầu ra vào cuối tệp thay vì ghi đè.
- `-i`, `--ignore-interrupts`: Bỏ qua tín hiệu ngắt.
- `--help`: Hiển thị thông tin trợ giúp về lệnh tee.
- `--version`: Hiển thị phiên bản của lệnh tee.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `tee`:

1. Ghi đầu ra của lệnh `echo` vào tệp:
   ```bash
   echo "Hello, World!" | tee output.txt
   ```

2. Ghi đầu ra vào nhiều tệp:
   ```bash
   echo "Logging data" | tee file1.txt file2.txt
   ```

3. Thêm đầu ra vào tệp hiện có:
   ```bash
   echo "Appending this line" | tee -a output.txt
   ```

4. Kết hợp với lệnh `grep` để lọc và ghi đầu ra:
   ```bash
   ps aux | grep bash | tee bash_processes.txt
   ```

## Tips
- Sử dụng tùy chọn `-a` để đảm bảo không ghi đè lên tệp hiện có khi bạn muốn thêm dữ liệu.
- Kết hợp `tee` với các lệnh khác trong pipeline để theo dõi và lưu trữ đầu ra đồng thời.
- Hãy cẩn thận với quyền truy cập tệp; đảm bảo bạn có quyền ghi vào tệp mà bạn đang cố gắng ghi.