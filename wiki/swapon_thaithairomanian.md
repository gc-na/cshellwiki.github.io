# [Linux] Bash swapon sử dụng: Kích hoạt vùng swap

## Overview
Lệnh `swapon` được sử dụng để kích hoạt các vùng swap trên hệ thống Linux. Swap là một không gian trên đĩa cứng được sử dụng để mở rộng bộ nhớ ảo, giúp hệ thống hoạt động mượt mà hơn khi bộ nhớ RAM đầy.

## Usage
Cú pháp cơ bản của lệnh `swapon` như sau:
```
swapon [options] [arguments]
```

## Common Options
- `-a`: Kích hoạt tất cả các vùng swap được chỉ định trong tệp `/etc/fstab`.
- `-s`: Hiển thị thông tin về các vùng swap hiện đang hoạt động.
- `--show`: Tương tự như `-s`, hiển thị thông tin chi tiết về các vùng swap.

## Common Examples
Kích hoạt tất cả các vùng swap được định nghĩa trong tệp `/etc/fstab`:
```bash
swapon -a
```

Hiển thị thông tin về các vùng swap hiện tại:
```bash
swapon -s
```

Kích hoạt một tệp swap cụ thể:
```bash
swapon /path/to/swapfile
```

## Tips
- Đảm bảo rằng tệp swap đã được tạo và có quyền truy cập thích hợp trước khi sử dụng lệnh `swapon`.
- Sử dụng lệnh `swapoff` để vô hiệu hóa vùng swap khi không cần thiết, giúp tối ưu hóa hiệu suất hệ thống.
- Kiểm tra thường xuyên tình trạng bộ nhớ và swap để đảm bảo hệ thống hoạt động hiệu quả.