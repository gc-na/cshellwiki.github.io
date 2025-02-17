# [Linux] Bash df sử dụng: Kiểm tra dung lượng ổ đĩa

## Overview
Lệnh `df` dùng để hiển thị thông tin về dung lượng ổ đĩa và không gian trống trên các hệ thống tệp. Nó giúp người dùng theo dõi và quản lý dung lượng lưu trữ trên máy tính của họ.

## Usage
Cú pháp cơ bản của lệnh `df` như sau:
```
df [options] [arguments]
```

## Common Options
- `-h`: Hiển thị dung lượng theo định dạng dễ đọc (KB, MB, GB).
- `-T`: Hiển thị loại hệ thống tệp.
- `-a`: Hiển thị tất cả các hệ thống tệp, bao gồm cả những hệ thống tệp không sử dụng.
- `-i`: Hiển thị thông tin về inode thay vì dung lượng.

## Common Examples
1. Hiển thị thông tin dung lượng ổ đĩa cơ bản:
   ```bash
   df
   ```

2. Hiển thị dung lượng ổ đĩa với định dạng dễ đọc:
   ```bash
   df -h
   ```

3. Hiển thị loại hệ thống tệp:
   ```bash
   df -T
   ```

4. Hiển thị thông tin về inode:
   ```bash
   df -i
   ```

5. Hiển thị tất cả các hệ thống tệp:
   ```bash
   df -a
   ```

## Tips
- Sử dụng tùy chọn `-h` để dễ dàng đọc và hiểu thông tin dung lượng.
- Thường xuyên kiểm tra dung lượng ổ đĩa để tránh tình trạng đầy ổ đĩa, điều này có thể ảnh hưởng đến hiệu suất hệ thống.
- Kết hợp lệnh `df` với lệnh `grep` để tìm kiếm thông tin cụ thể về ổ đĩa.