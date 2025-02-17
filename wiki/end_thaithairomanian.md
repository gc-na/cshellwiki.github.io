# [Linux] Bash end sử dụng: Kết thúc một tiến trình

## Overview
Lệnh `end` trong Bash được sử dụng để kết thúc một tiến trình đang chạy. Lệnh này rất hữu ích khi bạn cần dừng một chương trình hoặc một tác vụ đang chiếm dụng tài nguyên hệ thống.

## Usage
Cú pháp cơ bản của lệnh `end` như sau:
```bash
end [options] [arguments]
```

## Common Options
- `-p`: Chỉ định PID của tiến trình cần kết thúc.
- `-f`: Kết thúc một tiến trình mà không cần xác nhận.
- `-h`: Hiển thị thông tin trợ giúp về lệnh `end`.

## Common Examples
- Kết thúc một tiến trình bằng PID:
```bash
end -p 1234
```
- Kết thúc tất cả các tiến trình của một người dùng:
```bash
end -u username
```
- Kết thúc một tiến trình mà không cần xác nhận:
```bash
end -f -p 5678
```

## Tips
- Luôn kiểm tra danh sách tiến trình đang chạy trước khi sử dụng lệnh `end` để tránh kết thúc nhầm tiến trình quan trọng.
- Sử dụng lệnh `ps` để tìm PID của tiến trình bạn muốn kết thúc.
- Hãy cẩn thận khi sử dụng tùy chọn `-f`, vì nó sẽ không yêu cầu xác nhận trước khi kết thúc tiến trình.