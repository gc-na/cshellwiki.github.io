# [Linux] Bash pidstat Cách sử dụng: Theo dõi hiệu suất tiến trình

## Overview
Lệnh `pidstat` là một công cụ trong Linux dùng để theo dõi và báo cáo thông tin về hiệu suất của các tiến trình đang chạy trên hệ thống. Nó cung cấp thông tin chi tiết như mức sử dụng CPU, bộ nhớ và nhiều thông số khác cho từng tiến trình.

## Usage
Cú pháp cơ bản của lệnh `pidstat` như sau:

```bash
pidstat [options] [arguments]
```

## Common Options
- `-h`: Hiển thị tiêu đề cho các cột.
- `-r`: Hiển thị thông tin về mức sử dụng bộ nhớ.
- `-u`: Hiển thị thông tin về mức sử dụng CPU.
- `-p <pid>`: Theo dõi một tiến trình cụ thể theo PID.
- `-t`: Hiển thị thông tin cho tất cả các luồng của tiến trình.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `pidstat`:

1. **Theo dõi mức sử dụng CPU của tất cả các tiến trình:**
   ```bash
   pidstat -u
   ```

2. **Theo dõi mức sử dụng bộ nhớ của tất cả các tiến trình:**
   ```bash
   pidstat -r
   ```

3. **Theo dõi một tiến trình cụ thể theo PID:**
   ```bash
   pidstat -p 1234
   ```

4. **Theo dõi thông tin cho tất cả các luồng của một tiến trình:**
   ```bash
   pidstat -t -p 1234
   ```

5. **Theo dõi mức sử dụng CPU và bộ nhớ theo khoảng thời gian:**
   ```bash
   pidstat -u -r 1 5
   ```
   (Lệnh này sẽ hiển thị thông tin mỗi giây trong 5 giây.)

## Tips
- Sử dụng tùy chọn `-h` để dễ dàng đọc tiêu đề cột khi xuất thông tin.
- Kết hợp `pidstat` với các lệnh khác như `grep` để lọc thông tin theo nhu cầu.
- Theo dõi tiến trình quan trọng trong thời gian thực để phát hiện vấn đề hiệu suất kịp thời.