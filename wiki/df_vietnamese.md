# [Linux] Bash df Cách sử dụng: Kiểm tra dung lượng ổ đĩa

## Overview
Lệnh `df` trong Bash được sử dụng để hiển thị thông tin về dung lượng ổ đĩa và mức sử dụng của các hệ thống tệp. Nó cho phép người dùng theo dõi dung lượng còn lại và dung lượng đã sử dụng trên các phân vùng khác nhau của hệ thống.

## Usage
Cú pháp cơ bản của lệnh `df` như sau:
```
df [options] [arguments]
```

## Common Options
- `-h`: Hiển thị dung lượng theo định dạng dễ đọc (KB, MB, GB).
- `-T`: Hiển thị loại hệ thống tệp.
- `-a`: Hiển thị tất cả các hệ thống tệp, bao gồm cả các hệ thống tệp 0 dung lượng.
- `-i`: Hiển thị thông tin về inode thay vì dung lượng.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `df`:

1. Hiển thị thông tin dung lượng ổ đĩa cơ bản:
   ```bash
   df
   ```

2. Hiển thị thông tin với định dạng dễ đọc:
   ```bash
   df -h
   ```

3. Hiển thị thông tin loại hệ thống tệp:
   ```bash
   df -T
   ```

4. Hiển thị thông tin về tất cả các hệ thống tệp:
   ```bash
   df -a
   ```

5. Hiển thị thông tin inode:
   ```bash
   df -i
   ```

## Tips
- Sử dụng tùy chọn `-h` để dễ dàng đọc thông tin dung lượng, đặc biệt khi làm việc với các ổ đĩa lớn.
- Thường xuyên kiểm tra dung lượng ổ đĩa để tránh tình trạng đầy ổ đĩa, có thể gây ra sự cố cho hệ thống.
- Kết hợp `df` với các lệnh khác như `grep` để lọc thông tin theo nhu cầu cụ thể.