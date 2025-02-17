# [Linux] Bash docker cách sử dụng: Quản lý container và hình ảnh

## Overview
Lệnh `docker` được sử dụng để quản lý các container và hình ảnh trong môi trường Docker. Nó cho phép người dùng tạo, khởi động, dừng và xóa các container, cũng như quản lý các hình ảnh Docker.

## Usage
Cú pháp cơ bản của lệnh docker như sau:
```bash
docker [options] [arguments]
```

## Common Options
- `run`: Tạo và khởi động một container mới.
- `ps`: Liệt kê tất cả các container đang chạy.
- `images`: Hiển thị danh sách các hình ảnh Docker có sẵn.
- `rm`: Xóa một hoặc nhiều container.
- `rmi`: Xóa một hoặc nhiều hình ảnh Docker.

## Common Examples
- **Khởi động một container mới từ một hình ảnh:**
```bash
docker run hello-world
```

- **Liệt kê các container đang chạy:**
```bash
docker ps
```

- **Liệt kê tất cả các container, bao gồm cả những container đã dừng:**
```bash
docker ps -a
```

- **Xóa một container cụ thể:**
```bash
docker rm <container_id>
```

- **Xóa một hình ảnh cụ thể:**
```bash
docker rmi <image_id>
```

## Tips
- Luôn kiểm tra các container đang chạy bằng lệnh `docker ps` để quản lý tốt hơn.
- Sử dụng `docker run -d` để chạy container ở chế độ nền.
- Thường xuyên dọn dẹp các container và hình ảnh không còn sử dụng để tiết kiệm dung lượng ổ đĩa.