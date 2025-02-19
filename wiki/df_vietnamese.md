# [Hệ điều hành] C Shell (csh) df Cách sử dụng: Kiểm tra dung lượng ổ đĩa

## Tổng quan
Lệnh `df` trong C Shell (csh) được sử dụng để hiển thị thông tin về dung lượng ổ đĩa và tình trạng sử dụng của các hệ thống tệp. Nó giúp người dùng theo dõi dung lượng còn lại và dung lượng đã sử dụng trên các phân vùng khác nhau.

## Cách sử dụng
Cú pháp cơ bản của lệnh `df` như sau:
```
df [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-h`: Hiển thị dung lượng theo định dạng dễ đọc (KB, MB, GB).
- `-T`: Hiển thị loại hệ thống tệp cho mỗi phân vùng.
- `-a`: Hiển thị tất cả các hệ thống tệp, bao gồm cả những hệ thống tệp không được gắn.
- `-i`: Hiển thị thông tin về số lượng inode thay vì dung lượng.

## Ví dụ phổ biến
- Hiển thị thông tin dung lượng ổ đĩa:
  ```csh
  df
  ```

- Hiển thị thông tin với định dạng dễ đọc:
  ```csh
  df -h
  ```

- Hiển thị loại hệ thống tệp:
  ```csh
  df -T
  ```

- Hiển thị tất cả các hệ thống tệp:
  ```csh
  df -a
  ```

- Hiển thị thông tin về inode:
  ```csh
  df -i
  ```

## Mẹo
- Sử dụng tùy chọn `-h` để dễ dàng đọc và hiểu dung lượng ổ đĩa.
- Kiểm tra định kỳ dung lượng ổ đĩa để tránh tình trạng đầy ổ đĩa, có thể gây ra sự cố cho hệ thống.
- Kết hợp lệnh `df` với các lệnh khác như `grep` để lọc thông tin cụ thể mà bạn cần.