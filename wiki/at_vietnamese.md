# [Linux] Bash tại at: Lập lịch thực thi lệnh

## Overview
Lệnh `at` trong Bash cho phép người dùng lập lịch để thực thi một lệnh hoặc một tập lệnh vào một thời điểm cụ thể trong tương lai. Điều này rất hữu ích cho việc tự động hóa các tác vụ mà bạn muốn thực hiện mà không cần phải can thiệp thủ công.

## Usage
Cú pháp cơ bản của lệnh `at` như sau:
```
at [options] [time]
```

## Common Options
- `-f FILE`: Chỉ định một tệp chứa lệnh cần thực thi.
- `-m`: Gửi email thông báo khi lệnh đã được thực thi.
- `-q QUEUE`: Chỉ định hàng đợi mà lệnh sẽ được thêm vào.
- `-l`: Liệt kê các tác vụ đã được lập lịch.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `at`:

1. **Lập lịch một lệnh để thực thi ngay sau 5 phút:**
   ```bash
   echo "echo 'Hello, World!'" | at now + 5 minutes
   ```

2. **Lập lịch một lệnh vào lúc 3 giờ chiều hôm nay:**
   ```bash
   echo "backup.sh" | at 15:00
   ```

3. **Lập lịch một lệnh từ một tệp:**
   ```bash
   at -f myscript.sh 10:00
   ```

4. **Liệt kê các tác vụ đã được lập lịch:**
   ```bash
   at -l
   ```

## Tips
- Hãy chắc chắn rằng dịch vụ `atd` đang chạy trên hệ thống của bạn để lệnh `at` hoạt động.
- Sử dụng tùy chọn `-m` để nhận thông báo qua email khi lệnh đã được thực thi, giúp bạn theo dõi các tác vụ đã lập lịch.
- Kiểm tra lại thời gian và ngày tháng khi lập lịch để tránh nhầm lẫn và đảm bảo lệnh được thực thi đúng thời điểm mong muốn.