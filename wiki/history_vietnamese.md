# [Linux] Bash history cách sử dụng: Lưu trữ và truy xuất lệnh đã thực hiện

## Overview
Lệnh `history` trong Bash cho phép người dùng xem lại danh sách các lệnh đã thực hiện trong phiên làm việc của họ. Điều này rất hữu ích để nhanh chóng truy cập lại các lệnh mà bạn đã sử dụng trước đó mà không cần phải gõ lại chúng.

## Usage
Cú pháp cơ bản của lệnh `history` như sau:

```bash
history [options] [arguments]
```

## Common Options
- `-c`: Xóa toàn bộ lịch sử lệnh.
- `-d offset`: Xóa lệnh tại vị trí `offset` trong lịch sử.
- `n`: Hiển thị `n` lệnh gần nhất.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `history`:

1. **Hiển thị toàn bộ lịch sử lệnh:**
   ```bash
   history
   ```

2. **Hiển thị 10 lệnh gần nhất:**
   ```bash
   history 10
   ```

3. **Xóa lệnh tại vị trí thứ 5 trong lịch sử:**
   ```bash
   history -d 5
   ```

4. **Xóa toàn bộ lịch sử lệnh:**
   ```bash
   history -c
   ```

## Tips
- Bạn có thể sử dụng phím mũi tên lên và xuống để di chuyển qua các lệnh đã thực hiện mà không cần phải gõ lại.
- Để thực thi lại một lệnh từ lịch sử, bạn có thể nhập `!n`, trong đó `n` là số thứ tự của lệnh trong danh sách lịch sử.
- Hãy thường xuyên kiểm tra và xóa lịch sử lệnh để bảo mật thông tin nhạy cảm.