# [Linux] Bash logrotate: Quản lý tệp nhật ký

## Overview
Lệnh `logrotate` được sử dụng để quản lý và xoay vòng các tệp nhật ký trên hệ thống Linux. Nó giúp tự động hóa quá trình nén, xóa hoặc chuyển đổi các tệp nhật ký để tiết kiệm không gian lưu trữ và duy trì hiệu suất hệ thống.

## Usage
Cú pháp cơ bản của lệnh `logrotate` như sau:

```bash
logrotate [options] [arguments]
```

## Common Options
Dưới đây là một số tùy chọn phổ biến của `logrotate` cùng với giải thích ngắn gọn:

- `-f`: Buộc thực hiện xoay vòng nhật ký ngay cả khi không cần thiết.
- `-s`: Chỉ định tệp trạng thái để theo dõi các tệp nhật ký đã được xoay vòng.
- `-v`: Hiển thị thông tin chi tiết về quá trình xoay vòng nhật ký.
- `-d`: Chạy trong chế độ gỡ lỗi mà không thực hiện bất kỳ thay đổi nào.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng `logrotate`:

1. **Chạy logrotate với tệp cấu hình mặc định**:
   ```bash
   logrotate /etc/logrotate.conf
   ```

2. **Buộc xoay vòng nhật ký ngay cả khi không cần thiết**:
   ```bash
   logrotate -f /etc/logrotate.conf
   ```

3. **Chạy logrotate trong chế độ gỡ lỗi**:
   ```bash
   logrotate -d /etc/logrotate.conf
   ```

4. **Sử dụng tệp trạng thái tùy chỉnh**:
   ```bash
   logrotate -s /var/lib/logrotate/status /etc/logrotate.conf
   ```

## Tips
- Đảm bảo cấu hình tệp `/etc/logrotate.conf` và các tệp trong thư mục `/etc/logrotate.d/` đúng cách để tránh mất dữ liệu nhật ký.
- Thực hiện kiểm tra định kỳ để đảm bảo rằng các tệp nhật ký được xoay vòng đúng cách và không chiếm quá nhiều không gian lưu trữ.
- Sử dụng tùy chọn `-v` để theo dõi quá trình xoay vòng nhật ký và phát hiện các vấn đề nếu có.