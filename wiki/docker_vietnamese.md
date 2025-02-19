# [Hệ điều hành] C Shell (csh) docker sử dụng: Quản lý container

## Tổng quan
Lệnh `docker` được sử dụng để quản lý và điều phối các container trong môi trường ảo hóa. Nó cho phép người dùng tạo, chạy, dừng và xóa các container, cũng như quản lý hình ảnh và mạng.

## Cú pháp
Cú pháp cơ bản của lệnh docker như sau:
```
docker [tùy chọn] [tham số]
```

## Tùy chọn phổ biến
- `run`: Tạo và chạy một container mới.
- `ps`: Liệt kê các container đang chạy.
- `stop`: Dừng một hoặc nhiều container.
- `rm`: Xóa một hoặc nhiều container.
- `images`: Liệt kê các hình ảnh có sẵn trên hệ thống.

## Ví dụ phổ biến
- Tạo và chạy một container mới từ hình ảnh:
  ```bash
  docker run hello-world
  ```

- Liệt kê các container đang chạy:
  ```bash
  docker ps
  ```

- Dừng một container cụ thể:
  ```bash
  docker stop <container_id>
  ```

- Xóa một container:
  ```bash
  docker rm <container_id>
  ```

- Liệt kê các hình ảnh có sẵn:
  ```bash
  docker images
  ```

## Mẹo
- Luôn kiểm tra trạng thái của container bằng lệnh `docker ps` trước khi thực hiện các thao tác dừng hoặc xóa.
- Sử dụng `docker logs <container_id>` để xem nhật ký của container, giúp bạn theo dõi hoạt động và xử lý sự cố.
- Đặt tên cho container khi tạo bằng cách sử dụng tùy chọn `--name` để dễ dàng quản lý hơn.