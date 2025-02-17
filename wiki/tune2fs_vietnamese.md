# [Linux] Bash tune2fs cách sử dụng: Thay đổi các tham số của hệ thống tệp ext2/ext3/ext4

## Overview
Lệnh `tune2fs` được sử dụng để điều chỉnh các tham số của hệ thống tệp ext2, ext3 và ext4. Nó cho phép người dùng thay đổi các thuộc tính như kích thước khối, số lượng inode, và các thông số khác để tối ưu hóa hiệu suất hoặc khả năng lưu trữ của hệ thống tệp.

## Usage
Cú pháp cơ bản của lệnh `tune2fs` như sau:
```bash
tune2fs [options] [arguments]
```

## Common Options
- `-c <num>`: Đặt số lần kiểm tra hệ thống tệp trước khi tự động kiểm tra.
- `-i <interval>`: Đặt khoảng thời gian giữa các lần kiểm tra tự động.
- `-m <reserved-blocks>`: Đặt tỷ lệ phần trăm không gian đĩa được giữ lại cho người dùng root.
- `-O <feature>`: Kích hoạt một tính năng mới cho hệ thống tệp.
- `-L <label>`: Đặt nhãn cho hệ thống tệp.

## Common Examples
- Để thiết lập số lần kiểm tra hệ thống tệp trước khi kiểm tra tự động:
```bash
tune2fs -c 20 /dev/sda1
```

- Để đặt khoảng thời gian kiểm tra tự động là 6 tháng:
```bash
tune2fs -i 6m /dev/sda1
```

- Để giữ lại 5% không gian đĩa cho người dùng root:
```bash
tune2fs -m 5 /dev/sda1
```

- Để kích hoạt tính năng `dir_index` cho hệ thống tệp:
```bash
tune2fs -O dir_index /dev/sda1
```

- Để đặt nhãn cho hệ thống tệp:
```bash
tune2fs -L "MyLabel" /dev/sda1
```

## Tips
- Trước khi sử dụng `tune2fs`, hãy chắc chắn rằng hệ thống tệp không đang được sử dụng hoặc đã được gỡ bỏ để tránh mất dữ liệu.
- Sử dụng lệnh `tune2fs -l /dev/sda1` để xem các thông tin hiện tại của hệ thống tệp trước khi thực hiện bất kỳ thay đổi nào.
- Hãy cẩn thận khi thay đổi các tham số, vì một số thay đổi có thể ảnh hưởng đến hiệu suất và tính ổn định của hệ thống tệp.