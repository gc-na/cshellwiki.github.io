# [Linux] Bash helm cách sử dụng: Quản lý ứng dụng Kubernetes

## Tổng quan
Lệnh `helm` là một công cụ quản lý gói cho Kubernetes, giúp người dùng dễ dàng cài đặt, nâng cấp và quản lý các ứng dụng chạy trên cụm Kubernetes. Helm sử dụng khái niệm "charts" để định nghĩa cấu hình và các tài nguyên cần thiết cho ứng dụng.

## Cách sử dụng
Cú pháp cơ bản của lệnh helm như sau:
```bash
helm [options] [arguments]
```

## Các tùy chọn phổ biến
- `install`: Cài đặt một chart.
- `upgrade`: Nâng cấp một chart đã cài đặt.
- `uninstall`: Gỡ bỏ một chart.
- `list`: Liệt kê các release đã cài đặt.
- `repo`: Quản lý các kho chứa chart.

## Ví dụ thường gặp
- Cài đặt một chart:
```bash
helm install my-release stable/nginx
```

- Nâng cấp một release:
```bash
helm upgrade my-release stable/nginx
```

- Gỡ bỏ một release:
```bash
helm uninstall my-release
```

- Liệt kê các release đã cài đặt:
```bash
helm list
```

- Thêm một kho chứa chart mới:
```bash
helm repo add my-repo https://example.com/charts
```

## Mẹo
- Luôn kiểm tra phiên bản của chart trước khi cài đặt hoặc nâng cấp để đảm bảo tính tương thích.
- Sử dụng các giá trị tùy chỉnh bằng cách thêm `--set` để điều chỉnh cấu hình theo nhu cầu của bạn.
- Thường xuyên cập nhật kho chứa chart bằng lệnh `helm repo update` để có các phiên bản mới nhất.