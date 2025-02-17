# [Linux] Bash tail cách sử dụng: Hiển thị nội dung cuối của tệp

## Tổng quan
Lệnh `tail` trong Bash được sử dụng để hiển thị các dòng cuối cùng của một tệp. Đây là một công cụ hữu ích để theo dõi các tệp log hoặc kiểm tra dữ liệu mới được thêm vào.

## Cách sử dụng
Cú pháp cơ bản của lệnh `tail` như sau:

```bash
tail [tùy chọn] [tệp]
```

## Tùy chọn phổ biến
- `-n [số]`: Hiển thị số dòng cuối cùng được chỉ định từ tệp.
- `-f`: Theo dõi tệp theo thời gian thực, hiển thị các dòng mới khi chúng được thêm vào.
- `-c [số]`: Hiển thị số byte cuối cùng được chỉ định từ tệp.

## Ví dụ phổ biến
- Hiển thị 10 dòng cuối cùng của tệp `log.txt`:

```bash
tail log.txt
```

- Hiển thị 20 dòng cuối cùng của tệp `data.txt`:

```bash
tail -n 20 data.txt
```

- Theo dõi tệp `access.log` theo thời gian thực:

```bash
tail -f access.log
```

- Hiển thị 50 byte cuối cùng của tệp `file.txt`:

```bash
tail -c 50 file.txt
```

## Mẹo
- Sử dụng `tail -f` để theo dõi các tệp log trong thời gian thực, điều này rất hữu ích cho việc giám sát hoạt động của ứng dụng.
- Kết hợp `tail` với các lệnh khác như `grep` để tìm kiếm thông tin cụ thể trong các dòng cuối cùng của tệp.
- Nếu bạn muốn dừng theo dõi tệp với `tail -f`, chỉ cần nhấn `Ctrl + C`.