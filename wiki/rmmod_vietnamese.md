# [Linux] Bash rmmod: Xóa mô-đun kernel

## Overview
Lệnh `rmmod` được sử dụng để xóa hoặc gỡ bỏ một mô-đun kernel đã được tải vào hệ thống. Mô-đun kernel là các phần mở rộng cho kernel Linux, cho phép thêm chức năng mà không cần biên dịch lại kernel.

## Usage
Cú pháp cơ bản của lệnh `rmmod` như sau:
```
rmmod [options] [arguments]
```

## Common Options
- `-f`: Buộc gỡ bỏ mô-đun ngay cả khi nó đang được sử dụng.
- `-n`: Không hiển thị thông báo lỗi nếu mô-đun không tồn tại.
- `--help`: Hiển thị hướng dẫn sử dụng lệnh.
- `--version`: Hiển thị thông tin phiên bản của lệnh.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `rmmod`:

1. Gỡ bỏ một mô-đun cụ thể:
   ```bash
   rmmod my_module
   ```

2. Buộc gỡ bỏ một mô-đun ngay cả khi nó đang được sử dụng:
   ```bash
   rmmod -f my_module
   ```

3. Hiển thị hướng dẫn sử dụng lệnh:
   ```bash
   rmmod --help
   ```

4. Kiểm tra phiên bản của lệnh `rmmod`:
   ```bash
   rmmod --version
   ```

## Tips
- Trước khi gỡ bỏ một mô-đun, hãy đảm bảo rằng không có tiến trình nào đang sử dụng mô-đun đó để tránh lỗi.
- Sử dụng tùy chọn `-f` một cách cẩn thận, vì nó có thể gây ra sự không ổn định cho hệ thống nếu mô-đun đang được sử dụng.
- Kiểm tra danh sách các mô-đun đang hoạt động bằng lệnh `lsmod` trước khi thực hiện gỡ bỏ.