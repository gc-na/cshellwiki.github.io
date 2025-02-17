# [Linux] Bash minikube Sử dụng: Quản lý cụm Kubernetes cục bộ

## Tổng quan
Minikube là một công cụ giúp bạn dễ dàng triển khai và quản lý một cụm Kubernetes cục bộ trên máy tính của mình. Nó cho phép bạn thử nghiệm và phát triển ứng dụng trên Kubernetes mà không cần phải thiết lập một cụm phức tạp.

## Cách sử dụng
Cú pháp cơ bản của lệnh minikube như sau:
```
minikube [options] [arguments]
```

## Các tùy chọn phổ biến
- `start`: Khởi động cụm minikube.
- `stop`: Dừng cụm minikube đang chạy.
- `delete`: Xóa cụm minikube.
- `status`: Kiểm tra trạng thái của cụm minikube.
- `dashboard`: Mở giao diện người dùng web của Kubernetes.

## Ví dụ phổ biến
- Khởi động cụm minikube:
  ```bash
  minikube start
  ```

- Dừng cụm minikube:
  ```bash
  minikube stop
  ```

- Xóa cụm minikube:
  ```bash
  minikube delete
  ```

- Kiểm tra trạng thái cụm:
  ```bash
  minikube status
  ```

- Mở dashboard Kubernetes:
  ```bash
  minikube dashboard
  ```

## Mẹo
- Hãy chắc chắn rằng bạn đã cài đặt VirtualBox hoặc một trình ảo hóa khác trước khi khởi động minikube.
- Sử dụng `minikube update-check` để kiểm tra xem có phiên bản mới của minikube hay không.
- Thử nghiệm với các tùy chọn cấu hình như `--cpus` và `--memory` để tối ưu hóa hiệu suất cụm của bạn.