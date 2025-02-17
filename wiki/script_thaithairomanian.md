# [Linux] Bash script sử dụng: Ghi lại phiên làm việc của terminal

## Overview
Lệnh `script` trong Bash được sử dụng để ghi lại tất cả các hoạt động trong một phiên làm việc của terminal. Khi bạn chạy lệnh này, mọi đầu vào và đầu ra của terminal sẽ được lưu vào một tệp, cho phép bạn xem lại hoặc chia sẻ phiên làm việc của mình sau này.

## Usage
Cú pháp cơ bản của lệnh `script` là:

```bash
script [options] [arguments]
```

## Common Options
- `-a`: Thêm đầu ra vào tệp đã tồn tại thay vì ghi đè.
- `-f`: Hiển thị đầu ra ngay lập tức (flush output).
- `-t`: Ghi lại thời gian cho mỗi dòng đầu ra, hữu ích cho việc phân tích.
- `-q`: Chạy trong chế độ im lặng, không hiển thị thông báo bắt đầu và kết thúc.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `script`:

1. **Ghi lại phiên làm việc vào tệp `session.log`:**
   ```bash
   script session.log
   ```

2. **Ghi lại phiên làm việc và thêm vào tệp đã tồn tại:**
   ```bash
   script -a session.log
   ```

3. **Ghi lại phiên làm việc với đầu ra hiển thị ngay lập tức:**
   ```bash
   script -f session.log
   ```

4. **Ghi lại phiên làm việc và ghi lại thời gian:**
   ```bash
   script -t 2> timing.log session.log
   ```

## Tips
- Hãy nhớ kiểm tra tệp ghi lại sau khi hoàn thành phiên làm việc để đảm bảo rằng tất cả thông tin cần thiết đã được ghi lại.
- Sử dụng tùy chọn `-q` nếu bạn không muốn thấy thông báo bắt đầu và kết thúc, giúp bạn có một phiên làm việc sạch sẽ hơn.
- Nếu bạn cần chia sẻ phiên làm việc của mình, hãy nén tệp ghi lại để dễ dàng gửi qua email hoặc tải lên.