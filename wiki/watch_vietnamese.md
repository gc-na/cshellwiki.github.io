# [Linux] Bash watch cách sử dụng: Theo dõi lệnh trong thời gian thực

## Overview
Lệnh `watch` trong Bash cho phép người dùng theo dõi sự thay đổi của kết quả lệnh trong một khoảng thời gian nhất định. Nó tự động thực hiện lại lệnh mà bạn chỉ định và hiển thị kết quả mới nhất trên màn hình, giúp bạn dễ dàng quan sát các thay đổi.

## Usage
Cú pháp cơ bản của lệnh `watch` như sau:

```bash
watch [options] [arguments]
```

## Common Options
- `-n <seconds>`: Chỉ định khoảng thời gian (tính bằng giây) giữa các lần thực hiện lệnh.
- `-d`: Làm nổi bật sự khác biệt giữa các lần thực hiện lệnh.
- `-t`: Tắt tiêu đề hiển thị trên màn hình.
- `-x`: Chạy lệnh với các tham số được truyền vào.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `watch`:

1. Theo dõi sự thay đổi của thư mục hiện tại:
   ```bash
   watch -n 2 ls -l
   ```

2. Theo dõi trạng thái của một dịch vụ (ví dụ: nginx):
   ```bash
   watch -n 5 systemctl status nginx
   ```

3. Theo dõi sự thay đổi trong file log:
   ```bash
   watch -d tail -n 10 /var/log/syslog
   ```

4. Theo dõi dung lượng ổ đĩa:
   ```bash
   watch -n 10 df -h
   ```

## Tips
- Sử dụng tùy chọn `-d` để dễ dàng nhận biết sự thay đổi giữa các lần thực hiện lệnh.
- Nếu bạn chỉ cần theo dõi một lệnh trong một khoảng thời gian ngắn, hãy sử dụng tùy chọn `-n` với giá trị nhỏ.
- Để tạm dừng lệnh `watch`, bạn có thể nhấn `Ctrl + C` để dừng theo dõi.