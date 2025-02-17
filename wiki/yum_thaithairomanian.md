# [Linux] Bash yum sử dụng: Quản lý gói phần mềm

## Overview
Lệnh `yum` (Yellowdog Updater, Modified) là một công cụ quản lý gói cho các hệ điều hành dựa trên RPM, như CentOS và Fedora. Nó cho phép người dùng cài đặt, cập nhật, xóa và quản lý các gói phần mềm một cách dễ dàng.

## Usage
Cú pháp cơ bản của lệnh `yum` như sau:
```
yum [options] [arguments]
```

## Common Options
- `install`: Cài đặt một gói phần mềm.
- `remove`: Gỡ bỏ một gói phần mềm.
- `update`: Cập nhật các gói đã cài đặt.
- `search`: Tìm kiếm gói phần mềm theo tên hoặc mô tả.
- `info`: Hiển thị thông tin chi tiết về một gói phần mềm.

## Common Examples
- Cài đặt một gói phần mềm:
  ```bash
  yum install httpd
  ```
- Gỡ bỏ một gói phần mềm:
  ```bash
  yum remove httpd
  ```
- Cập nhật tất cả các gói đã cài đặt:
  ```bash
  yum update
  ```
- Tìm kiếm một gói phần mềm:
  ```bash
  yum search nginx
  ```
- Hiển thị thông tin về một gói phần mềm:
  ```bash
  yum info httpd
  ```

## Tips
- Luôn kiểm tra các gói có sẵn trước khi cài đặt bằng cách sử dụng `yum search`.
- Sử dụng `yum clean all` để xóa bộ nhớ cache và giải phóng dung lượng đĩa.
- Để cập nhật chỉ một gói cụ thể, hãy sử dụng `yum update [tên-gói]` thay vì cập nhật tất cả.