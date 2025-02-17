# [Linux] Bash helm sử dụng: Quản lý ứng dụng Kubernetes

## Overview
Lệnh `helm` là một công cụ quản lý gói cho Kubernetes, cho phép người dùng dễ dàng cài đặt, nâng cấp và quản lý các ứng dụng trên cụm Kubernetes. Helm sử dụng khái niệm "charts" để đóng gói các ứng dụng, giúp việc triển khai trở nên đơn giản và hiệu quả hơn.

## Usage
Cú pháp cơ bản của lệnh helm như sau:
```bash
helm [options] [arguments]
```

## Common Options
- `install`: Cài đặt một chart mới.
- `upgrade`: Nâng cấp một chart đã cài đặt.
- `uninstall`: Gỡ bỏ một chart đã cài đặt.
- `list`: Liệt kê các release đã cài đặt.
- `repo`: Quản lý các kho lưu trữ chart.

## Common Examples
1. **Cài đặt một chart mới:**
   ```bash
   helm install my-release stable/mysql
   ```
   Lệnh này cài đặt chart MySQL từ kho lưu trữ stable với tên release là `my-release`.

2. **Nâng cấp một release đã cài đặt:**
   ```bash
   helm upgrade my-release stable/mysql
   ```
   Lệnh này nâng cấp release `my-release` với chart MySQL.

3. **Gỡ bỏ một release:**
   ```bash
   helm uninstall my-release
   ```
   Lệnh này gỡ bỏ release `my-release` khỏi cụm Kubernetes.

4. **Liệt kê các release đã cài đặt:**
   ```bash
   helm list
   ```
   Lệnh này hiển thị danh sách tất cả các release đã được cài đặt.

5. **Quản lý kho lưu trữ chart:**
   ```bash
   helm repo add my-repo https://charts.example.com
   ```
   Lệnh này thêm một kho lưu trữ chart mới có tên là `my-repo`.

## Tips
- Luôn kiểm tra các chart có sẵn trong kho lưu trữ trước khi cài đặt bằng lệnh `helm search repo`.
- Sử dụng `--dry-run` để kiểm tra các thay đổi mà không thực hiện cài đặt thực tế.
- Đọc tài liệu của từng chart để hiểu rõ các tùy chọn cấu hình có sẵn.