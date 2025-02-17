# [Linux] Bash swapon Cách sử dụng: Kích hoạt không gian swap

## Overview
Lệnh `swapon` được sử dụng để kích hoạt không gian swap trên hệ thống Linux. Swap là một phần của bộ nhớ ảo, cho phép hệ điều hành sử dụng không gian trên đĩa cứng như một phần mở rộng của bộ nhớ RAM, giúp cải thiện hiệu suất khi bộ nhớ RAM đầy.

## Usage
Cú pháp cơ bản của lệnh `swapon` như sau:

```bash
swapon [options] [arguments]
```

## Common Options
- `-a`: Kích hoạt tất cả các không gian swap được định nghĩa trong tệp `/etc/fstab`.
- `-s`: Hiển thị thông tin về các không gian swap hiện tại.
- `--show`: Tương tự như `-s`, hiển thị thông tin chi tiết về không gian swap.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `swapon`:

### Kích hoạt không gian swap từ tệp fstab
```bash
swapon -a
```

### Hiển thị thông tin về không gian swap
```bash
swapon -s
```

### Kích hoạt một tệp swap cụ thể
```bash
swapon /path/to/swapfile
```

### Kích hoạt không gian swap và hiển thị thông tin
```bash
swapon --show
```

## Tips
- Đảm bảo rằng không gian swap đã được tạo và định dạng đúng trước khi sử dụng lệnh `swapon`.
- Sử dụng `swapon -s` để kiểm tra tình trạng không gian swap hiện tại và xác định xem có cần thêm không gian swap hay không.
- Để tắt không gian swap, bạn có thể sử dụng lệnh `swapoff` theo cú pháp tương tự.