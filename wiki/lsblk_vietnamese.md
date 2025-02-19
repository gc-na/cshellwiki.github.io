# [Hệ điều hành Linux] C Shell (csh) lsblk Cách sử dụng: [hiển thị thông tin về các thiết bị lưu trữ]

## Tổng quan
Lệnh `lsblk` được sử dụng để liệt kê thông tin về các thiết bị lưu trữ trong hệ thống, bao gồm cả ổ đĩa cứng, ổ đĩa USB và phân vùng. Lệnh này giúp người dùng dễ dàng theo dõi và quản lý các thiết bị lưu trữ.

## Cách sử dụng
Cú pháp cơ bản của lệnh `lsblk` như sau:
```
lsblk [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`: Hiển thị tất cả các thiết bị, bao gồm cả những thiết bị không có phân vùng.
- `-f`: Hiển thị thông tin về hệ thống tập tin.
- `-l`: Hiển thị danh sách theo định dạng hàng.
- `-o`: Chỉ định các cột thông tin cần hiển thị.
- `-p`: Hiển thị đường dẫn đầy đủ của thiết bị.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `lsblk`:

1. Liệt kê tất cả các thiết bị lưu trữ:
   ```bash
   lsblk
   ```

2. Hiển thị thông tin chi tiết về hệ thống tập tin:
   ```bash
   lsblk -f
   ```

3. Hiển thị danh sách theo định dạng hàng:
   ```bash
   lsblk -l
   ```

4. Chỉ định các cột thông tin cần hiển thị, ví dụ: tên, loại và kích thước:
   ```bash
   lsblk -o NAME,TYPE,SIZE
   ```

5. Hiển thị đường dẫn đầy đủ của các thiết bị:
   ```bash
   lsblk -p
   ```

## Mẹo
- Sử dụng tùy chọn `-f` để nhanh chóng kiểm tra hệ thống tập tin của các thiết bị.
- Kết hợp `lsblk` với các lệnh khác như `grep` để lọc thông tin theo nhu cầu.
- Thường xuyên kiểm tra thông tin thiết bị lưu trữ để phát hiện sớm các vấn đề tiềm ẩn.