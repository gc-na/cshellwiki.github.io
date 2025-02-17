# [Linux] Bash last lệnh: Xem lịch sử đăng nhập của người dùng

## Overview
Lệnh `last` trong Bash được sử dụng để hiển thị danh sách các lần đăng nhập gần đây của người dùng trên hệ thống. Nó cung cấp thông tin về thời gian, địa chỉ IP và thời gian đăng xuất của người dùng.

## Usage
Cú pháp cơ bản của lệnh `last` như sau:

```bash
last [options] [arguments]
```

## Common Options
- `-a`: Hiển thị địa chỉ IP hoặc tên máy của người dùng.
- `-n [number]`: Giới hạn số lượng bản ghi được hiển thị (mặc định là 10).
- `-R`: Không hiển thị tên máy.
- `-x`: Hiển thị thông tin về các phiên làm việc và các lần khởi động lại hệ thống.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `last`:

1. **Xem lịch sử đăng nhập gần đây**:
   ```bash
   last
   ```

2. **Giới hạn số lượng bản ghi hiển thị**:
   ```bash
   last -n 5
   ```

3. **Hiển thị địa chỉ IP của người dùng**:
   ```bash
   last -a
   ```

4. **Hiển thị thông tin về các phiên làm việc**:
   ```bash
   last -x
   ```

5. **Xem lịch sử đăng nhập của một người dùng cụ thể**:
   ```bash
   last username
   ```

## Tips
- Sử dụng tùy chọn `-n` để chỉ định số lượng bản ghi bạn muốn xem, giúp bạn dễ dàng quản lý thông tin.
- Kết hợp với lệnh `grep` để tìm kiếm thông tin cụ thể, ví dụ: `last | grep username`.
- Để theo dõi các lần khởi động lại hệ thống, hãy sử dụng tùy chọn `-x` để có cái nhìn tổng quan hơn.