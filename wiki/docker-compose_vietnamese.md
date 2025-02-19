# [Hệ điều hành] C Shell (csh) docker-compose Sử dụng: Quản lý các dịch vụ Docker

## Tổng quan
Lệnh `docker-compose` được sử dụng để định nghĩa và chạy nhiều container Docker như một ứng dụng. Nó cho phép người dùng dễ dàng cấu hình và quản lý các dịch vụ liên quan đến nhau thông qua một tệp cấu hình.

## Cách sử dụng
Cú pháp cơ bản của lệnh `docker-compose` như sau:
```csh
docker-compose [options] [arguments]
```

## Các tùy chọn phổ biến
- `up`: Khởi động các dịch vụ được định nghĩa trong tệp `docker-compose.yml`.
- `down`: Dừng và xóa các container, mạng và volume được tạo bởi `up`.
- `build`: Xây dựng lại các dịch vụ.
- `logs`: Hiển thị nhật ký của các container.
- `ps`: Liệt kê các container đang chạy.

## Ví dụ phổ biến
- Khởi động các dịch vụ:
```csh
docker-compose up
```

- Dừng và xóa các dịch vụ:
```csh
docker-compose down
```

- Xây dựng lại các dịch vụ:
```csh
docker-compose build
```

- Hiển thị nhật ký của các container:
```csh
docker-compose logs
```

- Liệt kê các container đang chạy:
```csh
docker-compose ps
```

## Mẹo
- Sử dụng tệp `.env` để quản lý các biến môi trường cho dự án của bạn.
- Thực hiện lệnh `docker-compose up -d` để chạy các dịch vụ ở chế độ nền.
- Đảm bảo rằng bạn đã cài đặt Docker và Docker Compose trước khi sử dụng lệnh này.