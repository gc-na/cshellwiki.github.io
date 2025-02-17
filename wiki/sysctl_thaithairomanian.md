# [Linux] Bash sysctl sử dụng: Quản lý tham số kernel

## Overview
Lệnh `sysctl` được sử dụng để xem và thay đổi các tham số của kernel trong hệ điều hành Linux. Nó cho phép người dùng điều chỉnh các thiết lập hệ thống mà không cần khởi động lại máy.

## Usage
Cú pháp cơ bản của lệnh `sysctl` như sau:
```bash
sysctl [options] [arguments]
```

## Common Options
- `-a`: Hiển thị tất cả các tham số kernel hiện tại.
- `-w`: Thay đổi giá trị của một tham số kernel.
- `-p`: Tải các tham số từ một tệp cấu hình.

## Common Examples
- Hiển thị tất cả các tham số kernel:
```bash
sysctl -a
```

- Thay đổi giá trị của một tham số kernel (ví dụ: tăng kích thước tối đa của các tệp mở):
```bash
sysctl -w fs.file-max=100000
```

- Tải các tham số kernel từ tệp cấu hình `/etc/sysctl.conf`:
```bash
sysctl -p
```

## Tips
- Trước khi thay đổi bất kỳ tham số nào, hãy chắc chắn rằng bạn hiểu tác động của nó đến hệ thống.
- Sử dụng lệnh `sysctl -a` để kiểm tra các tham số hiện tại trước khi thực hiện thay đổi.
- Để giữ các thay đổi sau khi khởi động lại, hãy thêm các tham số vào tệp `/etc/sysctl.conf`.