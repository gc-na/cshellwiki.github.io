# [Linux] Bash endsw: Kết thúc một tiến trình

## Overview
Lệnh `endsw` trong Bash được sử dụng để kết thúc một tiến trình đang chạy. Lệnh này rất hữu ích khi bạn cần dừng một tiến trình mà không cần phải khởi động lại hệ thống hoặc sử dụng các công cụ quản lý tiến trình khác.

## Usage
Cú pháp cơ bản của lệnh `endsw` như sau:
```
endsw [options] [arguments]
```

## Common Options
- `-h`, `--help`: Hiển thị thông tin trợ giúp về lệnh `endsw`.
- `-v`, `--version`: Hiển thị phiên bản của lệnh `endsw`.
- `-p`, `--pid`: Kết thúc tiến trình theo ID tiến trình (PID) được chỉ định.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `endsw`:

1. Kết thúc một tiến trình theo PID:
   ```bash
   endsw -p 1234
   ```

2. Hiển thị thông tin trợ giúp:
   ```bash
   endsw --help
   ```

3. Kết thúc nhiều tiến trình cùng lúc:
   ```bash
   endsw -p 1234 -p 5678
   ```

## Tips
- Luôn kiểm tra PID của tiến trình trước khi sử dụng `endsw` để tránh kết thúc nhầm tiến trình quan trọng.
- Sử dụng lệnh `ps` để liệt kê các tiến trình đang chạy và tìm PID của chúng.
- Nếu bạn không chắc chắn về việc kết thúc một tiến trình, hãy xem xét việc sử dụng lệnh `kill` với các tín hiệu khác nhau để kiểm soát tốt hơn.