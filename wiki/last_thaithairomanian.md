# [Linux] Bash last sử dụng: Hiển thị lịch sử đăng nhập của người dùng

## Overview
Lệnh `last` trong Bash được sử dụng để hiển thị lịch sử đăng nhập của người dùng trên hệ thống. Nó cho phép bạn xem ai đã đăng nhập, thời gian đăng nhập và thời gian đăng xuất, giúp theo dõi hoạt động của người dùng trên máy chủ.

## Usage
Cú pháp cơ bản của lệnh `last` như sau:

```bash
last [options] [arguments]
```

## Common Options
- `-a`: Hiển thị địa chỉ IP hoặc tên máy tính của người dùng.
- `-n <number>`: Chỉ định số lượng bản ghi lịch sử đăng nhập cần hiển thị.
- `-R`: Không hiển thị tên máy tính.
- `-x`: Hiển thị thông tin về các phiên làm việc và các sự kiện khởi động lại.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `last`:

1. Hiển thị toàn bộ lịch sử đăng nhập:
   ```bash
   last
   ```

2. Hiển thị 5 bản ghi đăng nhập gần đây nhất:
   ```bash
   last -n 5
   ```

3. Hiển thị địa chỉ IP của người dùng:
   ```bash
   last -a
   ```

4. Hiển thị thông tin về các phiên làm việc:
   ```bash
   last -x
   ```

## Tips
- Sử dụng tùy chọn `-n` để giới hạn số lượng bản ghi hiển thị, giúp bạn dễ dàng quản lý thông tin.
- Kết hợp với lệnh `grep` để tìm kiếm thông tin cụ thể về một người dùng:
  ```bash
  last | grep username
  ```
- Thường xuyên kiểm tra lịch sử đăng nhập để phát hiện các hoạt động đáng ngờ trên hệ thống của bạn.