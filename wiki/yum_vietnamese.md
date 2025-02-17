# [Linux] Bash yum cách sử dụng: Quản lý gói phần mềm

## Tổng quan
Lệnh `yum` (Yellowdog Updater Modified) là một công cụ quản lý gói trên các hệ điều hành dựa trên RPM, như CentOS và Fedora. Nó cho phép người dùng cài đặt, cập nhật, và gỡ bỏ các gói phần mềm một cách dễ dàng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `yum` như sau:
```
yum [options] [arguments]
```

## Các tùy chọn phổ biến
- `install`: Cài đặt gói phần mềm.
- `remove`: Gỡ bỏ gói phần mềm.
- `update`: Cập nhật gói phần mềm đã cài đặt.
- `search`: Tìm kiếm gói phần mềm trong kho lưu trữ.
- `info`: Hiển thị thông tin chi tiết về gói phần mềm.

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

- Tìm kiếm một gói phần mềm:
  ```bash
  yum search nginx
  ```

- Hiển thị thông tin về một gói phần mềm:
  ```bash
  yum info httpd
  ```

## Mẹo
- Luôn kiểm tra các gói có thể cập nhật bằng cách sử dụng `yum check-update` trước khi thực hiện cập nhật.
- Sử dụng `yum clean all` để dọn dẹp bộ nhớ cache và giải phóng không gian đĩa.
- Để cài đặt nhiều gói cùng lúc, bạn có thể liệt kê chúng cách nhau bằng dấu cách:
  ```bash
  yum install git vim curl
  ```