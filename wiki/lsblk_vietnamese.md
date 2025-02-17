# [Linux] Bash lsblk Cách sử dụng: Liệt kê thiết bị lưu trữ

## Tổng quan
Lệnh `lsblk` được sử dụng để liệt kê các thiết bị lưu trữ trong hệ thống, bao gồm cả ổ đĩa cứng, ổ USB và phân vùng. Lệnh này hiển thị thông tin chi tiết về các thiết bị, giúp người dùng dễ dàng quản lý và theo dõi tình trạng của các thiết bị lưu trữ.

## Cú pháp
Cú pháp cơ bản của lệnh `lsblk` như sau:
```
lsblk [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`, `--all`: Hiển thị tất cả các thiết bị, bao gồm cả những thiết bị không có phân vùng.
- `-f`, `--fs`: Hiển thị thông tin hệ thống tập tin của các thiết bị.
- `-l`, `--list`: Hiển thị danh sách các thiết bị theo dạng danh sách thay vì dạng cây.
- `-o`, `--output`: Chỉ định các cột thông tin cần hiển thị.
- `-p`, `--paths`: Hiển thị đường dẫn đầy đủ của các thiết bị.

## Ví dụ thường gặp
- Hiển thị danh sách tất cả các thiết bị lưu trữ:
  ```bash
  lsblk
  ```

- Hiển thị thông tin hệ thống tập tin của các thiết bị:
  ```bash
  lsblk -f
  ```

- Hiển thị danh sách theo dạng danh sách:
  ```bash
  lsblk -l
  ```

- Hiển thị các cột thông tin cụ thể, chẳng hạn như tên, kích thước và loại:
  ```bash
  lsblk -o NAME,SIZE,TYPE
  ```

## Mẹo
- Sử dụng tùy chọn `-p` để có được đường dẫn đầy đủ của các thiết bị, điều này có thể hữu ích khi bạn cần chỉ định thiết bị trong các lệnh khác.
- Kết hợp `lsblk` với các lệnh khác như `grep` để lọc thông tin theo nhu cầu cụ thể.
- Thường xuyên kiểm tra các thiết bị lưu trữ của bạn để đảm bảo rằng chúng hoạt động bình thường và không có vấn đề gì.