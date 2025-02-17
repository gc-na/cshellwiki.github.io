# [Linux] Bash hwclock cách sử dụng: Quản lý đồng hồ hệ thống

## Tổng quan
Lệnh `hwclock` được sử dụng để truy cập và điều chỉnh đồng hồ phần cứng (hardware clock) của hệ thống. Đồng hồ phần cứng là một bộ đếm thời gian độc lập với hệ điều hành, giúp duy trì thời gian ngay cả khi máy tính tắt nguồn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `hwclock` như sau:
```bash
hwclock [options] [arguments]
```

## Các tùy chọn phổ biến
- `--show`: Hiển thị thời gian hiện tại của đồng hồ phần cứng.
- `--set`: Thiết lập thời gian cho đồng hồ phần cứng.
- `--hctosys`: Đồng bộ hóa thời gian từ đồng hồ phần cứng sang đồng hồ hệ thống.
- `--systohc`: Đồng bộ hóa thời gian từ đồng hồ hệ thống sang đồng hồ phần cứng.
- `--utc`: Chỉ định rằng đồng hồ phần cứng đang sử dụng thời gian UTC.

## Ví dụ thường gặp
- Hiển thị thời gian hiện tại của đồng hồ phần cứng:
```bash
hwclock --show
```

- Thiết lập thời gian cho đồng hồ phần cứng:
```bash
hwclock --set --date="2023-10-01 12:00:00"
```

- Đồng bộ hóa thời gian từ đồng hồ phần cứng sang đồng hồ hệ thống:
```bash
hwclock --hctosys
```

- Đồng bộ hóa thời gian từ đồng hồ hệ thống sang đồng hồ phần cứng:
```bash
hwclock --systohc
```

- Thiết lập đồng hồ phần cứng sử dụng thời gian UTC:
```bash
hwclock --set --date="2023-10-01 12:00:00" --utc
```

## Mẹo
- Luôn kiểm tra thời gian của đồng hồ phần cứng sau khi khởi động lại hệ thống để đảm bảo rằng nó chính xác.
- Sử dụng tùy chọn `--utc` nếu bạn đang chạy nhiều hệ điều hành trên cùng một máy tính và muốn đồng bộ hóa thời gian.
- Đặt lịch trình tự động đồng bộ hóa thời gian giữa đồng hồ hệ thống và đồng hồ phần cứng để tránh sai lệch thời gian.