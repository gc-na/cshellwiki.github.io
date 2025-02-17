# [Linux] Bash host sử dụng: [truy vấn DNS]

## Overview
Lệnh `host` được sử dụng để truy vấn thông tin DNS (Domain Name System). Nó cho phép người dùng tìm kiếm địa chỉ IP của một tên miền hoặc tìm kiếm tên miền tương ứng với một địa chỉ IP.

## Usage
Cú pháp cơ bản của lệnh `host` như sau:
```bash
host [options] [arguments]
```

## Common Options
- `-a`: Hiển thị tất cả các thông tin DNS cho tên miền.
- `-t`: Chỉ định loại bản ghi DNS cần truy vấn (ví dụ: A, MX, CNAME).
- `-v`: Chạy lệnh ở chế độ chi tiết, hiển thị thêm thông tin về quá trình truy vấn.

## Common Examples
- Tìm địa chỉ IP của một tên miền:
```bash
host example.com
```

- Tìm tên miền tương ứng với một địa chỉ IP:
```bash
host 93.184.216.34
```

- Tìm bản ghi MX (Mail Exchange) của một tên miền:
```bash
host -t MX example.com
```

- Hiển thị tất cả thông tin DNS cho một tên miền:
```bash
host -a example.com
```

## Tips
- Sử dụng tùy chọn `-v` để có thêm thông tin chi tiết khi cần gỡ lỗi vấn đề DNS.
- Kết hợp lệnh `host` với các lệnh khác như `grep` để lọc kết quả dễ dàng hơn.
- Kiểm tra nhiều máy chủ DNS khác nhau bằng cách sử dụng tùy chọn `-r` để chỉ định máy chủ DNS cụ thể.