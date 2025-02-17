# [Bash dmesg Sử dụng: Hiển thị thông điệp hệ thống khởi động]

## Overview
Lệnh `dmesg` được sử dụng để hiển thị các thông điệp từ bộ đệm của kernel. Nó thường được sử dụng để kiểm tra các thông báo khởi động hệ thống và các sự kiện liên quan đến phần cứng.

## Usage
Cú pháp cơ bản của lệnh `dmesg` như sau:
```bash
dmesg [options] [arguments]
```

## Common Options
- `-C`: Xóa bộ đệm hiện tại.
- `-c`: Hiển thị thông điệp và sau đó xóa bộ đệm.
- `-n level`: Đặt mức độ thông báo mà bạn muốn hiển thị.
- `-T`: Hiển thị thời gian con người dễ đọc cho các thông điệp.

## Common Examples
- Hiển thị tất cả thông điệp từ bộ đệm kernel:
```bash
dmesg
```

- Hiển thị thông điệp với thời gian dễ đọc:
```bash
dmesg -T
```

- Xóa bộ đệm sau khi hiển thị thông điệp:
```bash
dmesg -c
```

- Đặt mức độ thông báo để chỉ hiển thị thông điệp lỗi:
```bash
dmesg -n 1
```

## Tips
- Sử dụng `dmesg | less` để dễ dàng cuộn qua các thông điệp dài.
- Kết hợp `dmesg` với `grep` để tìm kiếm thông điệp cụ thể, ví dụ: `dmesg | grep error`.
- Theo dõi các thông điệp mới bằng cách sử dụng `dmesg -w`, cho phép bạn xem các thông điệp mới khi chúng được ghi vào bộ đệm.