# [Hệ điều hành] C Shell (csh) htop: [quản lý tiến trình tương tác]

## Tổng quan
Lệnh `htop` là một công cụ quản lý tiến trình tương tác trong môi trường dòng lệnh. Nó cho phép người dùng theo dõi và quản lý các tiến trình đang chạy trên hệ thống một cách trực quan và dễ dàng hơn so với các công cụ khác như `top`.

## Cú pháp
Cú pháp cơ bản của lệnh `htop` như sau:
```
htop [tùy chọn] [tham số]
```

## Các tùy chọn phổ biến
- `-h`, `--help`: Hiển thị hướng dẫn sử dụng.
- `-u`, `--user`: Chỉ hiển thị các tiến trình của người dùng cụ thể.
- `-p`, `--pid`: Chỉ hiển thị các tiến trình với ID tiến trình cụ thể.
- `-s`, `--sort-key`: Sắp xếp các tiến trình theo khóa cụ thể.

## Các ví dụ phổ biến
- Chạy `htop` để mở giao diện quản lý tiến trình:
  ```bash
  htop
  ```

- Chỉ hiển thị các tiến trình của người dùng `username`:
  ```bash
  htop -u username
  ```

- Chỉ hiển thị tiến trình với ID tiến trình là 1234:
  ```bash
  htop -p 1234
  ```

- Sắp xếp các tiến trình theo mức sử dụng CPU:
  ```bash
  htop -s PERCENT_CPU
  ```

## Mẹo
- Sử dụng phím `F3` để tìm kiếm tiến trình cụ thể trong danh sách.
- Nhấn `F9` để gửi tín hiệu đến một tiến trình, cho phép bạn dừng hoặc kết thúc tiến trình đó.
- Bạn có thể sử dụng phím `F2` để truy cập vào menu cấu hình và tùy chỉnh giao diện của `htop` theo ý muốn.