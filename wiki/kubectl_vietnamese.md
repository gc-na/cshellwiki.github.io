# [Hệ điều hành] C Shell (csh) kubectl Cách sử dụng: Quản lý Kubernetes

## Tổng quan
Lệnh `kubectl` là công cụ dòng lệnh chính để quản lý các cụm Kubernetes. Nó cho phép người dùng thực hiện các thao tác như triển khai ứng dụng, kiểm tra trạng thái của các tài nguyên, và quản lý các cấu hình trong cụm Kubernetes.

## Cách sử dụng
Cú pháp cơ bản của lệnh `kubectl` như sau:
```
kubectl [options] [arguments]
```

## Các tùy chọn phổ biến
- `get`: Lấy thông tin về các tài nguyên trong cụm.
- `apply`: Áp dụng các thay đổi từ file cấu hình vào cụm.
- `delete`: Xóa tài nguyên khỏi cụm.
- `describe`: Hiển thị thông tin chi tiết về một tài nguyên cụ thể.
- `logs`: Xem nhật ký của một pod.

## Ví dụ phổ biến
- Lấy danh sách tất cả các pod trong namespace mặc định:
  ```bash
  kubectl get pods
  ```

- Áp dụng cấu hình từ file YAML:
  ```bash
  kubectl apply -f deployment.yaml
  ```

- Xóa một pod cụ thể:
  ```bash
  kubectl delete pod my-pod
  ```

- Hiển thị thông tin chi tiết về một dịch vụ:
  ```bash
  kubectl describe service my-service
  ```

- Xem nhật ký của một pod:
  ```bash
  kubectl logs my-pod
  ```

## Mẹo
- Sử dụng `kubectl get all` để lấy thông tin về tất cả các tài nguyên trong namespace hiện tại.
- Thêm tùy chọn `-n <namespace>` để chỉ định namespace cụ thể khi thực hiện các lệnh.
- Sử dụng `--watch` để theo dõi sự thay đổi của tài nguyên theo thời gian thực.