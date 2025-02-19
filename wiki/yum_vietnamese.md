# [Hệ điều hành Linux] C Shell (csh) yum <Sử dụng yum>: Quản lý gói phần mềm

## Tổng quan
Lệnh `yum` (Yellowdog Updater Modified) là một công cụ quản lý gói phần mềm trên các hệ điều hành dựa trên RPM (Red Hat Package Manager). Nó cho phép người dùng cài đặt, cập nhật và gỡ bỏ các gói phần mềm một cách dễ dàng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `yum` như sau:
```
yum [options] [arguments]
```

## Các tùy chọn phổ biến
- `install`: Cài đặt gói phần mềm.
- `remove`: Gỡ bỏ gói phần mềm.
- `update`: Cập nhật gói phần mềm đã cài đặt.
- `list`: Liệt kê các gói phần mềm có sẵn hoặc đã cài đặt.
- `search`: Tìm kiếm gói phần mềm theo tên hoặc mô tả.

## Ví dụ thường gặp
- Cài đặt một gói phần mềm:
  ```bash
  yum install httpd
  ```
  
- Gỡ bỏ một gói phần mềm:
  ```bash
  yum remove httpd
  ```

- Cập nhật tất cả các gói phần mềm:
  ```bash
  yum update
  ```

- Liệt kê các gói phần mềm đã cài đặt:
  ```bash
  yum list installed
  ```

- Tìm kiếm một gói phần mềm:
  ```bash
  yum search nginx
  ```

## Mẹo
- Luôn kiểm tra các gói phần mềm có sẵn trước khi cài đặt để tránh xung đột.
- Sử dụng `yum clean all` để dọn dẹp bộ nhớ cache của yum, giúp tiết kiệm không gian lưu trữ.
- Đọc tài liệu hoặc sử dụng `yum --help` để tìm hiểu thêm về các tùy chọn và chức năng của lệnh.