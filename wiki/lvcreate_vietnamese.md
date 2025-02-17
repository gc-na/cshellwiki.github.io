# [Linux] Bash lvcreate Cách sử dụng: Tạo Logical Volume trong LVM

## Overview
Lệnh `lvcreate` được sử dụng để tạo Logical Volume (LV) trong Logical Volume Management (LVM) trên hệ điều hành Linux. Lệnh này cho phép người dùng phân chia và quản lý không gian lưu trữ một cách linh hoạt hơn.

## Usage
Cú pháp cơ bản của lệnh `lvcreate` như sau:

```bash
lvcreate [options] [arguments]
```

## Common Options
Dưới đây là một số tùy chọn phổ biến của lệnh `lvcreate`:

- `-n, --name <name>`: Đặt tên cho Logical Volume mới.
- `-L, --size <size>`: Xác định kích thước của Logical Volume.
- `-l, --extents <number>`: Chỉ định số lượng extents cho Logical Volume.
- `-m, --mirrors <number>`: Tạo số lượng bản sao cho Logical Volume.
- `-Z, --zero n`: Xác định có nên ghi đè bằng không vào Logical Volume hay không.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `lvcreate`:

1. Tạo một Logical Volume mới có tên là `my_volume` với kích thước 10GB:

   ```bash
   lvcreate -n my_volume -L 10G my_volume_group
   ```

2. Tạo một Logical Volume mới với kích thước được chỉ định bằng số lượng extents:

   ```bash
   lvcreate -n my_volume -l 100 my_volume_group
   ```

3. Tạo một Logical Volume với 2 bản sao:

   ```bash
   lvcreate -n my_volume -L 10G -m 1 my_volume_group
   ```

4. Tạo một Logical Volume và không ghi đè bằng không:

   ```bash
   lvcreate -n my_volume -L 10G -Z n my_volume_group
   ```

## Tips
- Trước khi tạo Logical Volume, hãy đảm bảo rằng bạn đã tạo một Volume Group (VG) và có đủ không gian trống.
- Sử dụng tùy chọn `-m` để tạo bản sao cho Logical Volume nhằm tăng cường độ tin cậy và khả năng phục hồi.
- Kiểm tra trạng thái của Logical Volume sau khi tạo bằng lệnh `lvdisplay` để đảm bảo mọi thứ hoạt động như mong đợi.