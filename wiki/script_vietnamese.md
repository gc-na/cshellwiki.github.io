# [Linux] Bash script Sử dụng: Ghi lại phiên làm việc

## Overview
Lệnh `script` trong Bash được sử dụng để ghi lại một phiên làm việc trong terminal. Khi bạn chạy lệnh này, tất cả các đầu ra và đầu vào của terminal sẽ được lưu vào một tệp tin, cho phép bạn xem lại hoặc chia sẻ phiên làm việc sau này.

## Usage
Cú pháp cơ bản của lệnh `script` như sau:
```
script [options] [arguments]
```

## Common Options
- `-a`: Thêm nội dung vào tệp đã tồn tại thay vì ghi đè.
- `-f`: Hiển thị đầu ra ngay lập tức, không chờ đến khi phiên làm việc kết thúc.
- `-q`: Chạy lệnh mà không hiển thị thông báo khởi động.
- `-t`: Ghi lại thời gian thực hiện các lệnh trong phiên làm việc.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `script`:

1. **Ghi lại phiên làm việc mặc định**:
   ```bash
   script
   ```
   Lệnh này sẽ bắt đầu ghi lại phiên làm việc và lưu vào tệp `typescript`.

2. **Ghi lại phiên làm việc vào tệp cụ thể**:
   ```bash
   script mysession.log
   ```
   Phiên làm việc sẽ được ghi vào tệp `mysession.log`.

3. **Ghi lại phiên làm việc và thêm vào tệp đã tồn tại**:
   ```bash
   script -a mysession.log
   ```
   Lệnh này sẽ thêm nội dung mới vào tệp `mysession.log` thay vì ghi đè.

4. **Ghi lại phiên làm việc với hiển thị đầu ra ngay lập tức**:
   ```bash
   script -f mysession.log
   ```
   Phiên làm việc sẽ được ghi lại và hiển thị ngay lập tức.

## Tips
- Luôn kiểm tra tệp ghi lại sau khi kết thúc phiên làm việc để đảm bảo rằng mọi thứ đã được ghi lại chính xác.
- Sử dụng tùy chọn `-q` nếu bạn không muốn thấy thông báo khởi động, giúp phiên làm việc của bạn gọn gàng hơn.
- Nếu bạn cần ghi lại thời gian thực hiện các lệnh, hãy sử dụng tùy chọn `-t` để có thông tin chi tiết hơn.