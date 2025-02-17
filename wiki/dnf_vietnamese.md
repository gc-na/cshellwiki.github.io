# [Linux] Bash dnf Cách sử dụng: Quản lý gói phần mềm

## Tổng quan
Lệnh `dnf` (Dandified YUM) là một công cụ quản lý gói phần mềm trên các hệ điều hành dựa trên RPM như Fedora, CentOS và RHEL. Nó cho phép người dùng cài đặt, cập nhật, xóa và quản lý các gói phần mềm một cách dễ dàng và hiệu quả.

## Cách sử dụng
Cú pháp cơ bản của lệnh `dnf` như sau:
```
dnf [options] [arguments]
```

## Tùy chọn phổ biến
- `install`: Cài đặt gói phần mềm.
- `remove`: Gỡ bỏ gói phần mềm.
- `update`: Cập nhật gói phần mềm đã cài đặt.
- `search`: Tìm kiếm gói phần mềm.
- `info`: Hiển thị thông tin chi tiết về gói phần mềm.
- `list`: Liệt kê các gói đã cài đặt hoặc có sẵn.

## Ví dụ phổ biến
- Cài đặt một gói phần mềm:
  ```bash
  dnf install vim
  ```

- Gỡ bỏ một gói phần mềm:
  ```bash
  dnf remove vim
  ```

- Cập nhật tất cả các gói phần mềm:
  ```bash
  dnf update
  ```

- Tìm kiếm một gói phần mềm:
  ```bash
  dnf search httpd
  ```

- Hiển thị thông tin về một gói phần mềm:
  ```bash
  dnf info httpd
  ```

## Mẹo
- Luôn cập nhật danh sách gói trước khi cài đặt bằng cách sử dụng `dnf makecache`.
- Sử dụng `dnf history` để xem lại lịch sử các lệnh đã thực hiện.
- Kết hợp với `--assumeyes` để tự động xác nhận các yêu cầu trong quá trình cài đặt hoặc gỡ bỏ:
  ```bash
  dnf install vim --assumeyes
  ```