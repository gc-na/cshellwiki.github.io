# [Linux] Bash kubectl Sử dụng: Quản lý Kubernetes

## Overview
`kubectl` là công cụ dòng lệnh chính để quản lý các cụm Kubernetes. Nó cho phép người dùng tương tác với API của Kubernetes để triển khai ứng dụng, kiểm tra trạng thái của các tài nguyên, và thực hiện nhiều tác vụ quản lý khác.

## Usage
Cú pháp cơ bản của lệnh `kubectl` như sau:
```
kubectl [options] [arguments]
```

## Common Options
- `get`: Lấy thông tin về các tài nguyên trong cụm.
- `apply`: Áp dụng các thay đổi từ tệp cấu hình vào cụm.
- `delete`: Xóa tài nguyên khỏi cụm.
- `describe`: Hiển thị thông tin chi tiết về một tài nguyên cụ thể.
- `logs`: Xem nhật ký của một pod.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng `kubectl`:

1. **Lấy danh sách các pod trong cụm:**
   ```bash
   kubectl get pods
   ```

2. **Áp dụng cấu hình từ tệp YAML:**
   ```bash
   kubectl apply -f deployment.yaml
   ```

3. **Xóa một pod cụ thể:**
   ```bash
   kubectl delete pod my-pod
   ```

4. **Hiển thị thông tin chi tiết về một dịch vụ:**
   ```bash
   kubectl describe service my-service
   ```

5. **Xem nhật ký của một pod:**
   ```bash
   kubectl logs my-pod
   ```

## Tips
- Sử dụng `kubectl get all` để lấy thông tin về tất cả các tài nguyên trong cụm.
- Thêm `-n <namespace>` để chỉ định không gian tên khi làm việc với các tài nguyên trong không gian tên cụ thể.
- Sử dụng `--watch` để theo dõi các thay đổi trong thời gian thực cho một tài nguyên.
- Thực hành sử dụng `kubectl explain <resource>` để tìm hiểu thêm về các tài nguyên và trường của chúng.