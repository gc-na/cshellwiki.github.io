# [Linux] Bash rpm cách sử dụng: Quản lý gói phần mềm

## Overview
Lệnh `rpm` (Red Hat Package Manager) được sử dụng để quản lý các gói phần mềm trên các hệ điều hành dựa trên Red Hat, như CentOS và Fedora. Nó cho phép người dùng cài đặt, gỡ bỏ, và quản lý các gói phần mềm một cách hiệu quả.

## Usage
Cú pháp cơ bản của lệnh `rpm` như sau:
```bash
rpm [options] [arguments]
```

## Common Options
- `-i`: Cài đặt một gói mới.
- `-e`: Gỡ bỏ một gói đã cài đặt.
- `-q`: Truy vấn thông tin về một gói.
- `-U`: Cập nhật một gói đã cài đặt.
- `--force`: Bỏ qua một số lỗi khi cài đặt hoặc gỡ bỏ gói.

## Common Examples
- Cài đặt một gói:
```bash
rpm -i package.rpm
```
- Gỡ bỏ một gói:
```bash
rpm -e package_name
```
- Truy vấn thông tin về một gói:
```bash
rpm -q package_name
```
- Cập nhật một gói:
```bash
rpm -U package.rpm
```

## Tips
- Luôn kiểm tra phiên bản của gói trước khi cài đặt hoặc cập nhật để tránh xung đột.
- Sử dụng tùy chọn `-v` để hiển thị thông tin chi tiết hơn trong quá trình cài đặt hoặc gỡ bỏ.
- Đảm bảo rằng bạn có quyền root hoặc sử dụng `sudo` khi thực hiện các thao tác cài đặt hoặc gỡ bỏ gói.