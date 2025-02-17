# [Linux] Bash swapoff cách sử dụng: Tắt phân vùng swap

## Tổng quan
Lệnh `swapoff` được sử dụng để tắt phân vùng hoặc tệp swap trên hệ thống Linux. Swap là một phần của bộ nhớ ảo, giúp hệ thống quản lý bộ nhớ hiệu quả hơn bằng cách sử dụng không gian trên đĩa cứng khi bộ nhớ RAM đầy.

## Cú pháp
Cú pháp cơ bản của lệnh `swapoff` như sau:
```bash
swapoff [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`: Tắt tất cả các phân vùng swap được chỉ định trong tệp `/etc/fstab`.
- `-e`: Bỏ qua các lỗi khi tắt swap.
- `-h`: Hiển thị thông tin trợ giúp về lệnh.

## Ví dụ thường gặp
- Tắt một phân vùng swap cụ thể:
```bash
swapoff /dev/sda2
```

- Tắt tất cả các phân vùng swap:
```bash
swapoff -a
```

- Tắt một tệp swap:
```bash
swapoff /swapfile
```

## Mẹo
- Trước khi tắt swap, hãy đảm bảo rằng hệ thống của bạn có đủ bộ nhớ RAM để xử lý các tác vụ hiện tại.
- Kiểm tra trạng thái swap trước khi tắt bằng lệnh `swapon --show` để xem các phân vùng swap đang hoạt động.
- Sử dụng lệnh `free -h` để theo dõi tình trạng bộ nhớ và swap của hệ thống.