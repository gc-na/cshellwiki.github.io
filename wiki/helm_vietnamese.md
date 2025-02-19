# [Hệ điều hành] C Shell (csh) helm <Sử dụng tương đương>: Quản lý biểu đồ Kubernetes

## Tổng quan
Lệnh `helm` được sử dụng để quản lý các biểu đồ (charts) trong Kubernetes, cho phép người dùng dễ dàng cài đặt, nâng cấp và quản lý các ứng dụng trong môi trường Kubernetes.

## Cách sử dụng
Cú pháp cơ bản của lệnh helm như sau:
```
helm [options] [arguments]
```

## Các tùy chọn phổ biến
- `install`: Cài đặt một biểu đồ mới.
- `upgrade`: Nâng cấp một biểu đồ đã cài đặt.
- `uninstall`: Gỡ bỏ một biểu đồ đã cài đặt.
- `list`: Liệt kê các biểu đồ đã cài đặt.
- `repo`: Quản lý các kho biểu đồ.

## Ví dụ phổ biến
- Cài đặt một biểu đồ:
  ```bash
  helm install my-release my-chart
  ```
  
- Nâng cấp một biểu đồ đã cài đặt:
  ```bash
  helm upgrade my-release my-chart
  ```

- Gỡ bỏ một biểu đồ:
  ```bash
  helm uninstall my-release
  ```

- Liệt kê các biểu đồ đã cài đặt:
  ```bash
  helm list
  ```

- Thêm một kho biểu đồ mới:
  ```bash
  helm repo add my-repo https://example.com/charts
  ```

## Mẹo
- Luôn kiểm tra phiên bản của biểu đồ trước khi nâng cấp để tránh các vấn đề không mong muốn.
- Sử dụng lệnh `helm template` để xem trước các tài nguyên Kubernetes mà biểu đồ sẽ tạo ra.
- Thường xuyên cập nhật kho biểu đồ bằng lệnh `helm repo update` để đảm bảo bạn có các phiên bản mới nhất.