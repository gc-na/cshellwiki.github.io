# [Linux] Bash vgextend Cách sử dụng: Mở rộng nhóm khối lượng

## Overview
Lệnh `vgextend` được sử dụng trong quản lý khối lượng logic (LVM) để mở rộng một nhóm khối lượng (volume group) bằng cách thêm một hoặc nhiều khối lượng vật lý (physical volume) vào nhóm đó. Điều này cho phép bạn tăng dung lượng lưu trữ của nhóm khối lượng hiện tại.

## Usage
Cú pháp cơ bản của lệnh `vgextend` như sau:
```
vgextend [options] [arguments]
```

## Common Options
- `-l, --extents <extents>`: Chỉ định số lượng extents mà bạn muốn thêm vào nhóm khối lượng.
- `-n, --noheadings`: Không hiển thị tiêu đề trong đầu ra.
- `-v, --verbose`: Hiển thị thông tin chi tiết trong quá trình thực hiện lệnh.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `vgextend`:

1. Mở rộng nhóm khối lượng bằng cách thêm một khối lượng vật lý:
   ```bash
   vgextend my_volume_group /dev/sdb1
   ```

2. Mở rộng nhóm khối lượng với nhiều khối lượng vật lý:
   ```bash
   vgextend my_volume_group /dev/sdb1 /dev/sdc1
   ```

3. Mở rộng nhóm khối lượng và hiển thị thông tin chi tiết:
   ```bash
   vgextend -v my_volume_group /dev/sdb1
   ```

## Tips
- Trước khi mở rộng nhóm khối lượng, hãy đảm bảo rằng các khối lượng vật lý bạn muốn thêm đã được định dạng và sẵn sàng sử dụng.
- Sử dụng tùy chọn `-v` để theo dõi quá trình thực hiện lệnh, điều này có thể hữu ích trong việc phát hiện lỗi.
- Kiểm tra dung lượng còn lại của nhóm khối lượng sau khi mở rộng để đảm bảo rằng bạn đã thêm đủ không gian cần thiết.