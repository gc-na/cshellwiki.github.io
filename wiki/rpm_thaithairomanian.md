# [Linux] Bash rpm sử dụng: Quản lý gói phần mềm trên hệ thống

## Overview
Lệnh `rpm` (Red Hat Package Manager) được sử dụng để quản lý gói phần mềm trên các hệ điều hành dựa trên Red Hat, như CentOS và Fedora. Nó cho phép người dùng cài đặt, gỡ bỏ, và quản lý các gói phần mềm đã được đóng gói dưới định dạng RPM.

## Usage
Cú pháp cơ bản của lệnh `rpm` như sau:
```bash
rpm [options] [arguments]
```

## Common Options
- `-i` : Cài đặt một gói RPM.
- `-e` : Gỡ bỏ một gói RPM.
- `-q` : Truy vấn thông tin về một gói đã cài đặt.
- `-U` : Cập nhật một gói RPM.
- `-v` : Hiển thị thông tin chi tiết trong quá trình thực hiện.
- `--nodeps` : Bỏ qua kiểm tra phụ thuộc khi cài đặt hoặc gỡ bỏ.

## Common Examples
- Cài đặt một gói RPM:
```bash
rpm -i package.rpm
```

- Gỡ bỏ một gói RPM:
```bash
rpm -e package_name
```

- Truy vấn thông tin về một gói đã cài đặt:
```bash
rpm -q package_name
```

- Cập nhật một gói RPM:
```bash
rpm -U package.rpm
```

- Hiển thị thông tin chi tiết khi cài đặt:
```bash
rpm -iv package.rpm -v
```

## Tips
- Luôn kiểm tra các phụ thuộc của gói trước khi cài đặt để tránh lỗi.
- Sử dụng tùy chọn `-q` để xác nhận xem gói đã được cài đặt hay chưa.
- Khi cập nhật gói, hãy đảm bảo rằng bạn đang sử dụng phiên bản mới nhất để tránh xung đột.