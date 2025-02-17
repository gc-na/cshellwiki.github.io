# [Linux] Bash logout cách sử dụng: Đăng xuất khỏi phiên làm việc

## Overview
Lệnh `logout` trong Bash được sử dụng để kết thúc phiên làm việc hiện tại của người dùng. Khi bạn thực hiện lệnh này, hệ thống sẽ đăng xuất người dùng khỏi shell hiện tại, thường là khi bạn đang làm việc trong một terminal hoặc một phiên SSH.

## Usage
Cú pháp cơ bản của lệnh `logout` như sau:

```
logout [options]
```

## Common Options
Lệnh `logout` không có nhiều tùy chọn, nhưng dưới đây là một số thông tin hữu ích:

- Không có tùy chọn: Lệnh `logout` thường không cần thêm tùy chọn nào và sẽ hoạt động ngay khi được gọi.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `logout`:

1. Đăng xuất khỏi phiên shell hiện tại:
   ```bash
   logout
   ```

2. Nếu bạn đang sử dụng một phiên SSH và muốn đăng xuất:
   ```bash
   logout
   ```

3. Trong một terminal, bạn có thể sử dụng lệnh `exit` tương đương với `logout`:
   ```bash
   exit
   ```

## Tips
- Hãy chắc chắn rằng bạn đã lưu lại tất cả công việc trước khi thực hiện lệnh `logout`, vì lệnh này sẽ đóng phiên làm việc và không thể khôi phục lại.
- Nếu bạn đang sử dụng nhiều tab trong terminal, hãy kiểm tra xem bạn đang ở tab nào trước khi đăng xuất để tránh mất dữ liệu không mong muốn.
- Lệnh `logout` thường được sử dụng trong các phiên làm việc không phải là root. Nếu bạn đang ở chế độ root, hãy sử dụng `exit` để thoát khỏi shell.