# [Linux] Bash free: Kiểm tra bộ nhớ hệ thống

## Overview
Lệnh `free` trong Bash được sử dụng để hiển thị thông tin về bộ nhớ hệ thống, bao gồm bộ nhớ RAM và swap. Nó cung cấp cái nhìn tổng quan về tình trạng sử dụng bộ nhớ, giúp người dùng theo dõi và quản lý tài nguyên hệ thống hiệu quả hơn.

## Usage
Cú pháp cơ bản của lệnh `free` như sau:
```bash
free [options] [arguments]
```

## Common Options
- `-h`: Hiển thị thông tin với định dạng dễ đọc (sử dụng đơn vị như MB, GB).
- `-m`: Hiển thị thông tin bộ nhớ theo megabyte.
- `-g`: Hiển thị thông tin bộ nhớ theo gigabyte.
- `-s <seconds>`: Cập nhật thông tin sau mỗi khoảng thời gian xác định (tính bằng giây).
- `-t`: Hiển thị tổng bộ nhớ (bao gồm cả bộ nhớ swap).

## Common Examples
- Hiển thị thông tin bộ nhớ cơ bản:
```bash
free
```

- Hiển thị thông tin bộ nhớ với định dạng dễ đọc:
```bash
free -h
```

- Hiển thị thông tin bộ nhớ theo megabyte:
```bash
free -m
```

- Hiển thị thông tin bộ nhớ theo gigabyte:
```bash
free -g
```

- Cập nhật thông tin bộ nhớ mỗi 5 giây:
```bash
free -s 5
```

- Hiển thị tổng bộ nhớ:
```bash
free -t
```

## Tips
- Sử dụng tùy chọn `-h` để dễ dàng đọc thông tin bộ nhớ, đặc biệt khi bạn làm việc với hệ thống có dung lượng lớn.
- Kết hợp lệnh `free` với lệnh `watch` để theo dõi tình trạng bộ nhớ theo thời gian thực:
```bash
watch free -h
```
- Kiểm tra thường xuyên tình trạng bộ nhớ để đảm bảo hệ thống hoạt động ổn định và hiệu quả.