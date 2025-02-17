# [Linux] Bash docker-compose cách sử dụng: Quản lý ứng dụng Docker dễ dàng

## Tổng quan
Lệnh `docker-compose` cho phép người dùng định nghĩa và chạy nhiều container Docker như một ứng dụng. Thông qua việc sử dụng tệp cấu hình, người dùng có thể dễ dàng thiết lập, khởi động và quản lý các dịch vụ liên quan đến ứng dụng của mình.

## Cách sử dụng
Cú pháp cơ bản của lệnh `docker-compose` như sau:

```bash
docker-compose [options] [arguments]
```

## Các tùy chọn phổ biến
- `up`: Khởi động các container theo cấu hình trong tệp `docker-compose.yml`.
- `down`: Dừng và xóa các container, mạng, và volume được tạo bởi `up`.
- `build`: Xây dựng lại các dịch vụ.
- `logs`: Hiển thị log của các container.
- `ps`: Liệt kê các container đang chạy.

## Ví dụ phổ biến
1. **Khởi động ứng dụng**:
   ```bash
   docker-compose up
   ```

2. **Khởi động ứng dụng ở chế độ nền**:
   ```bash
   docker-compose up -d
   ```

3. **Dừng ứng dụng**:
   ```bash
   docker-compose down
   ```

4. **Xem log của các container**:
   ```bash
   docker-compose logs
   ```

5. **Xây dựng lại các dịch vụ**:
   ```bash
   docker-compose build
   ```

## Mẹo
- Luôn kiểm tra tệp `docker-compose.yml` để đảm bảo rằng cấu hình của bạn chính xác trước khi khởi động.
- Sử dụng tùy chọn `-d` để chạy ứng dụng ở chế độ nền, giúp bạn tiếp tục sử dụng terminal mà không bị chặn.
- Thường xuyên kiểm tra log để theo dõi tình trạng của các container và phát hiện lỗi kịp thời.