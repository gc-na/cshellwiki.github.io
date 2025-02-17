# [Linux] Bash jobs sử dụng: Quản lý các tiến trình nền

## Overview
Lệnh `jobs` trong Bash được sử dụng để hiển thị danh sách các tiến trình nền đang chạy trong phiên làm việc hiện tại của người dùng. Nó cho phép bạn theo dõi và quản lý các tiến trình mà bạn đã khởi động trước đó.

## Usage
Cú pháp cơ bản của lệnh `jobs` như sau:
```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Hiển thị PID (Process ID) của các tiến trình.
- `-n`: Chỉ hiển thị các tiến trình đã thay đổi trạng thái kể từ lần gọi lệnh trước.
- `-p`: Chỉ hiển thị PID của các tiến trình.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `jobs`:

1. **Hiển thị danh sách các tiến trình nền:**
   ```bash
   jobs
   ```

2. **Hiển thị danh sách các tiến trình với PID:**
   ```bash
   jobs -l
   ```

3. **Hiển thị các tiến trình đã thay đổi trạng thái:**
   ```bash
   jobs -n
   ```

4. **Chỉ hiển thị PID của các tiến trình:**
   ```bash
   jobs -p
   ```

## Tips
- Sử dụng `bg` và `fg` để chuyển đổi giữa các tiến trình nền và tiến trình nền.
- Nếu bạn muốn dừng một tiến trình, bạn có thể sử dụng `Ctrl + Z` và sau đó sử dụng lệnh `jobs` để xem tiến trình đã dừng.
- Hãy nhớ rằng lệnh `jobs` chỉ hiển thị các tiến trình trong phiên làm việc hiện tại, do đó nếu bạn mở một phiên mới, bạn sẽ không thấy các tiến trình từ phiên trước.