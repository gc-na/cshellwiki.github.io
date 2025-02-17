# [Linux] Bash systemctl cách sử dụng: Quản lý dịch vụ hệ thống

## Tổng quan
Lệnh `systemctl` là một công cụ mạnh mẽ trong hệ thống Linux, được sử dụng để quản lý các dịch vụ và trạng thái của hệ thống. Nó cho phép bạn khởi động, dừng, khởi động lại, và kiểm tra trạng thái của các dịch vụ đang chạy trên hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `systemctl` như sau:
```
systemctl [options] [arguments]
```

## Các tùy chọn phổ biến
- `start`: Khởi động một dịch vụ.
- `stop`: Dừng một dịch vụ.
- `restart`: Khởi động lại một dịch vụ.
- `status`: Kiểm tra trạng thái của một dịch vụ.
- `enable`: Bật tự động khởi động dịch vụ khi hệ thống khởi động.
- `disable`: Tắt tự động khởi động dịch vụ khi hệ thống khởi động.

## Ví dụ thường gặp
- Khởi động một dịch vụ:
  ```bash
  systemctl start httpd
  ```
  
- Dừng một dịch vụ:
  ```bash
  systemctl stop httpd
  ```

- Khởi động lại một dịch vụ:
  ```bash
  systemctl restart httpd
  ```

- Kiểm tra trạng thái của một dịch vụ:
  ```bash
  systemctl status httpd
  ```

- Bật tự động khởi động dịch vụ khi hệ thống khởi động:
  ```bash
  systemctl enable httpd
  ```

- Tắt tự động khởi động dịch vụ khi hệ thống khởi động:
  ```bash
  systemctl disable httpd
  ```

## Mẹo
- Luôn kiểm tra trạng thái của dịch vụ sau khi thực hiện các thao tác khởi động hoặc dừng để đảm bảo rằng dịch vụ đang hoạt động như mong muốn.
- Sử dụng `systemctl list-units --type=service` để xem danh sách tất cả các dịch vụ đang chạy trên hệ thống.
- Để biết thêm thông tin chi tiết về một dịch vụ cụ thể, bạn có thể sử dụng `systemctl show [tên dịch vụ]`.