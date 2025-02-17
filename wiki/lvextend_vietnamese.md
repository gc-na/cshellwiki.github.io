# [Linux] Bash lvextend Cách sử dụng: Mở rộng kích thước Logical Volume

## Overview
Lệnh `lvextend` được sử dụng để mở rộng kích thước của một Logical Volume (LV) trong hệ thống quản lý Logical Volume (LVM). Khi bạn cần thêm dung lượng cho một volume đã tồn tại, `lvextend` là công cụ hữu ích giúp bạn thực hiện điều này một cách dễ dàng.

## Usage
Cú pháp cơ bản của lệnh `lvextend` như sau:

```bash
lvextend [options] [arguments]
```

## Common Options
Dưới đây là một số tùy chọn phổ biến của lệnh `lvextend`:

- `-L +size`: Thêm kích thước `size` vào volume hiện tại.
- `-L size`: Đặt kích thước mới cho volume.
- `-r`: Tự động mở rộng hệ thống tệp sau khi mở rộng volume.
- `-n`: Chỉ định tên của Logical Volume cần mở rộng.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng `lvextend`:

1. **Mở rộng một Logical Volume thêm 10GB:**
   ```bash
   lvextend -L +10G /dev/vg01/lv01
   ```

2. **Đặt kích thước mới cho Logical Volume là 50GB:**
   ```bash
   lvextend -L 50G /dev/vg01/lv01
   ```

3. **Mở rộng Logical Volume và tự động mở rộng hệ thống tệp:**
   ```bash
   lvextend -r -L +5G /dev/vg01/lv01
   ```

4. **Mở rộng Logical Volume với tên cụ thể:**
   ```bash
   lvextend -L +20G -n new_lv_name /dev/vg01/lv01
   ```

## Tips
- Trước khi mở rộng Logical Volume, hãy đảm bảo rằng bạn có đủ không gian trống trong Volume Group (VG).
- Sử dụng tùy chọn `-r` để tự động mở rộng hệ thống tệp, giúp tiết kiệm thời gian và công sức.
- Kiểm tra kích thước của Logical Volume sau khi mở rộng bằng lệnh `lvdisplay` để xác nhận rằng thay đổi đã được thực hiện thành công.